# Plan d'Action : Mise en Place et Sauvegarde du Serveur Web

## Sur l’ESXi
1. **Importer la VM serveur Web** :
   - Ouvrez votre client VMware ESXi.
   - Allez dans la section "Virtual Machines" et sélectionnez "Deploy OVF Template".
   - Choisissez le fichier `srv-web.ova` et suivez les étapes pour déployer la VM.

2. **Modifier l’adressage IP** :
   - Connectez-vous à la VM une fois déployée.
   - Modifiez le fichier de configuration réseau (ex. `/etc/network/interfaces` pour Debian/Ubuntu ou `/etc/sysconfig/network-scripts/ifcfg-eth0` pour CentOS/RedHat).
   - Attribuez l’adresse IP `172.16.X.200` et assurez-vous de définir la passerelle et les serveurs DNS correctement pour joindre le serveur AD.
   - Redémarrez le service réseau ou la VM.

3. **Vérifier que le service apache2 est en cours** :
   - Connectez-vous à la VM.
   - Exécutez `systemctl status apache2` (ou `httpd` pour CentOS/RedHat) pour vérifier que le service est actif.
   - Si le service n'est pas actif, démarrez-le avec `systemctl start apache2`.

## Sur `srv-ad1`
1. **Ajouter une entrée DNS type A pour `srv-web`** :
   - Ouvrez la console DNS sur le serveur AD.
   - Ajoutez un nouvel enregistrement A avec le nom `srv-web` pointant vers l’adresse IP `172.16.X.200`.

2. **Ajouter un CNAME `www` vers cet enregistrement A** :
   - Dans la même console DNS, ajoutez un enregistrement CNAME avec le nom `www` qui redirige vers `srv-web`.

3. **Tester depuis votre client** :
   - Depuis un client (ou même depuis le serveur web), utilisez `nslookup` ou `ping` pour vérifier la résolution des noms :
     ```bash
     nslookup srv-web
     nslookup www
     ```

## Sur `srv-backup`
1. **Faire une sauvegarde de `srv-web` avec Veeam** :
   - Ouvrez Veeam Backup & Replication.
   - Créez une tâche de sauvegarde pour la VM `srv-web`.
   - Lancez la sauvegarde et vérifiez qu’elle se termine correctement.

2. **Casser la VM et tenter une restauration** :
   - Éteignez la VM `srv-web` et supprimez un fichier critique ou changez sa configuration pour "casser" la VM.
   - Utilisez Veeam pour restaurer la VM à partir de la sauvegarde précédente et assurez-vous qu’elle fonctionne correctement après restauration.

## Sur `srv-web`
1. **Installer `rsync`** :
   - Connectez-vous à `srv-web`.
   - Installez `rsync` avec la commande :
     ```bash
     sudo apt-get install rsync
     ```
     ou
     ```bash
     sudo yum install rsync
     ```

2. **Monter le partage de fichier présent sur `srv-fic1`** :
   - Créez un point de montage, par exemple `/mnt/backup`.
   - Montez le partage réseau avec `mount` ou en modifiant `/etc/fstab` :
     ```bash
     sudo mount -t cifs //srv-fic1/share /mnt/backup -o username=utilisateur,password=motdepasse
     ```

3. **Avec Rsync, sauvegarder le contenu de `/etc/apache2/sites-available`** :
   - Exécutez la commande :
     ```bash
     rsync -av /etc/apache2/sites-available /mnt/backup/sites-available
     ```

4. **Avec Rsync, sauvegarder le contenu de `/var/www/`** :
   - Exécutez :
     ```bash
     rsync -av /var/www/ /mnt/backup/www
     ```

## Générer une panne et restaurer
1. **Sur `srv-web`, supprimer le fichier `/var/www/html/index.html`** :
   - Supprimez le fichier avec :
     ```bash
     sudo rm /var/www/html/index.html
     ```

2. **Tester le site web** :
   - Utilisez un navigateur ou `curl` pour vérifier que le site n’est plus accessible.

3. **Restaurer le fichier depuis la sauvegarde** :
   - Copiez le fichier depuis votre sauvegarde avec :
     ```bash
     rsync -av /mnt/backup/www/html/index.html /var/www/html/
     ```

4. **Tester le site web** :
   - Vérifiez à nouveau avec un navigateur ou `curl` que le site est bien restauré.

## Bonus : Automatisation avec un script Rsync
1. Créez un script shell pour automatiser les sauvegardes :
   ```bash
   #!/bin/bash
   BACKUP_DIR="/mnt/backup"
   DATE=$(date +%Y%m%d)

   # Sauvegarde de /etc/apache2/sites-available
   rsync -av /etc/apache2/sites-available $BACKUP_DIR/sites-available_$DATE

   # Sauvegarde de /var/www/
   rsync -av /var/www/ $BACKUP_DIR/www_$DATE
