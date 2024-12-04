# Liste complète des commandes Cisco

---

## 1. Commandes de base

| **Commande**                 | **Description**                                                                 | **Exemple**                          |
|-------------------------------|---------------------------------------------------------------------------------|--------------------------------------|
| `show clock`                 | Affiche l'heure et la date système.                                             | `Router# show clock`                |
| `hostname [nom]`             | Modifie le nom de l'appareil.                                                   | `Router(config)# hostname MonRouteur` |
| `reload`                     | Redémarre le périphérique.                                                      | `Router# reload`                    |
| `write erase`                | Efface la configuration sauvegardée (startup-config).                           | `Router# write erase`               |

---

## 2. Commandes de gestion de fichiers

| **Commande**                              | **Description**                                                                 | **Exemple**                                      |
|-------------------------------------------|---------------------------------------------------------------------------------|------------------------------------------------|
| `copy [source] [destination]`             | Copie des fichiers entre périphériques.                                         | `Router# copy running-config startup-config`   |
| `erase startup-config`                    | Supprime la configuration de démarrage.                                         | `Router# erase startup-config`                |
| `dir`                                     | Liste les fichiers présents dans un répertoire.                                 | `Router# dir flash:`                          |
| `delete [nom_fichier]`                    | Supprime un fichier spécifique.                                                | `Router# delete flash:config.old`             |

---

## 3. Configuration d'interface avancée

| **Commande**                   | **Description**                                                       | **Exemple**                                    |
|--------------------------------|-----------------------------------------------------------------------|-----------------------------------------------|
| `duplex [full|half|auto]`      | Configure le mode duplex d'une interface.                             | `Router(config-if)# duplex full`             |
| `speed [auto|10|100|1000]`     | Définit la vitesse d'une interface.                                   | `Router(config-if)# speed 100`               |
| `switchport mode trunk`        | Configure une interface en mode trunk.                                | `Switch(config-if)# switchport mode trunk`   |
| `switchport trunk allowed vlan [vlan_list]` | Spécifie les VLANs autorisés sur une interface trunk.                | `Switch(config-if)# switchport trunk allowed vlan 1,10,20` |

---

## 4. Configuration VLAN avancée

| **Commande**                        | **Description**                                                                   | **Exemple**                                        |
|-------------------------------------|-----------------------------------------------------------------------------------|--------------------------------------------------|
| `vlan database`                     | Permet de gérer les VLANs via une base de données dédiée.                         | `Switch# vlan database`                         |
| `show vlan brief`                   | Affiche un résumé de la configuration des VLANs.                                  | `Switch# show vlan brief`                       |
| `vlan [vlan_id]`                    | Crée un nouveau VLAN.                                                             | `Switch(config)# vlan 100`                      |
| `vtp mode [server|client|transparent]` | Configure le mode VTP (VLAN Trunking Protocol).                                  | `Switch(config)# vtp mode server`              |
| `vtp domain [nom_domaine]`          | Définit le domaine VTP.                                                           | `Switch(config)# vtp domain MonDomaine`         |

---

## 5. Routage avancé

| **Commande**                      | **Description**                                                                  | **Exemple**                                   |
|-----------------------------------|----------------------------------------------------------------------------------|----------------------------------------------|
| `ip default-gateway [ip]`         | Définit une passerelle par défaut pour les périphériques de niveau 2.            | `Switch(config)# ip default-gateway 192.168.1.1` |
| `show ip route`                   | Affiche la table de routage.                                                     | `Router# show ip route`                      |
| `router rip`                      | Active le protocole RIP.                                                         | `Router(config)# router rip`                 |
| `network [réseau]`                | Ajoute un réseau dans un processus de routage dynamique.                         | `Router(config-router)# network 10.0.0.0`    |
| `no auto-summary`                 | Désactive le résumé automatique des routes pour les protocoles comme RIP.        | `Router(config-router)# no auto-summary`     |

---

## 6. Sécurité avancée

| **Commande**                    | **Description**                                                               | **Exemple**                                      |
|---------------------------------|-------------------------------------------------------------------------------|------------------------------------------------|
| `service password-encryption`  | Crypte les mots de passe dans le fichier de configuration.                    | `Router(config)# service password-encryption` |
| `banner motd [texte]`           | Configure un message d'accueil pour les utilisateurs qui se connectent.      | `Router(config)# banner motd ^C Bienvenue! ^C` |
| `crypto key generate rsa`       | Génère des clés RSA pour SSH.                                                | `Router(config)# crypto key generate rsa`     |
| `username [nom] password [mot_de_passe]` | Crée un utilisateur avec mot de passe.                                     | `Router(config)# username admin password 1234` |

---

## 7. Commandes de QoS

| **Commande**                        | **Description**                                                                 | **Exemple**                                  |
|-------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------|
| `class-map [nom]`                   | Crée une classe pour la QoS.                                                    | `Router(config)# class-map VOIP`            |
| `policy-map [nom]`                  | Crée une politique QoS pour une classe.                                         | `Router(config)# policy-map PRIORITE_VOIP`  |
| `service-policy [nom]`              | Applique une politique QoS sur une interface.                                   | `Router(config-if)# service-policy input VOIP_POLICY` |

---

## 8. Dépannage avancé

| **Commande**                 | **Description**                                                                    | **Exemple**                             |
|------------------------------|------------------------------------------------------------------------------------|-----------------------------------------|
| `show interfaces [interface]` | Affiche les détails d'une interface spécifique, y compris les statistiques.       | `Router# show interfaces GigabitEthernet0/1` |
| `show ip protocols`          | Affiche les informations des protocoles de routage activés.                       | `Router# show ip protocols`            |
| `debug ip [protocole]`       | Active le débogage pour un protocole spécifique.                                   | `Router# debug ip rip`                 |
| `terminal monitor`           | Active l'affichage des messages de débogage sur le terminal.                      | `Router# terminal monitor`             |

---

## 9. Commandes VRF

| **Commande**                     | **Description**                                                                  | **Exemple**                               |
|----------------------------------|----------------------------------------------------------------------------------|------------------------------------------|
| `ip vrf [nom]`                   | Crée une instance de routage VRF.                                               | `Router(config)# ip vrf MON_VRF`         |
| `ip vrf forwarding [nom]`        | Associe une interface à un VRF.                                                 | `Router(config-if)# ip vrf forwarding MON_VRF` |

---

N'hésite pas à demander plus de détails sur une commande spécifique si besoin !
