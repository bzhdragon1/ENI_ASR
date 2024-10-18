# Énoncé

## Sur l’ESXi
- Importer la VM serveur Web depuis le fichier `srv-web.ova`.
- Modifier l’adressage IP de cette VM afin qu’elle réponde bien à l’adresse IP `172.16.X.200` et joint correctement la passerelle et le serveur AD.
- Vérifier que le service `apache2` est en cours.

## Sur `srv-ad1`
- Ajouter une entrée DNS type A pour `srv-web`.
- Ajouter un CNAME `www` vers cet enregistrement A.
- Tester depuis votre client.

## Sur `srv-backup`
- Faire une sauvegarde de `srv-web` avec Veeam.
- Casser la VM et tenter une restauration.

## Sur `srv-web`
- Installer `rsync`.
- Monter le partage de fichier présent sur `srv-fic1`.
- Avec `rsync`, sauvegarder le contenu de `/etc/apache2/sites-available`.
- Avec `rsync`, sauvegarder le contenu de `/var/www/`.

## Générer une panne et restaurer
- Sur `srv-web`, supprimer le fichier `/var/www/html/index.html`.
- Tester le site web.
- Restaurer le fichier depuis la sauvegarde.
- Tester le site web.

## Bonus
- Créer un script qui va automatiser les sauvegardes avec `rsync`.
