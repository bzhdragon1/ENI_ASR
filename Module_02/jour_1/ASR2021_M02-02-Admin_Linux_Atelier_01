# ENI Ecole Informatique

## Objectifs
- Installation d'un système RHEL graphique -> Oracle Linux en v8
- Image ISO : `OracleLinux-R8-U4-x86_64-dvd.iso`

## Prérequis
- Disposer d’une solution de virtualisation **VMware Workstation**

## Consignes
### Installez une distribution Oracle Linux avec les conditions suivantes :

#### Nom VMware
- **Nom VMware** : `M02-Wkstation`

#### Machine virtuelle
- **Taille de disque dur** : 40 Go
- **RAM** : 4096 Mo
- **CPU** : 2 processeurs avec 2 cœurs
- **Carte réseau** : en Bridge

#### Installation
- **Langue d'installation** : Français
- **Nom de l’hôte** : `srvclient`
- **Réseau** : DHCP (pour l’instant)

#### Partitionnement manuel
- `/boot` : Partitionnement normal (`sda1`), 500 MiB en XFS
- `Swap` : LVM, taille conseillée
- `/` : LVM, 20 GiB en XFS
- `/var` : LVM, 10 GiB en XFS
- `/home` : LVM utilisant l'espace restant en ext4

#### Choix des logiciels
- Environnement de bureau : **Gnome** (aucun autre logiciel supplémentaire)

### Créez un utilisateur
- **Nom de l'utilisateur** (non-administrateur) : `adminlo`

### Finalisation de l'installation
1. **Accepter la licence**
2. **Connecter le réseau filaire**
3. **Contrôler si les VMware Tools sont en fonctionnement** :
   ```bash
   ps ax | grep vmtoolsd
