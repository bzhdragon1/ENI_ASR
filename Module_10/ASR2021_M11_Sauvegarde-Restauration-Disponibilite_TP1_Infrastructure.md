# TP du Module 01 – Création de l'infrastructure

Ce TP concerne la création d'un environnement de maquettage basé sur VMware Workstation. Il simule un environnement mixte avec plusieurs machines virtuelles représentant des composants de sauvegarde, NAS, et autres serveurs.

## Informations Préliminaires

- **Durée estimée** : 2 à 3 heures
- **Prérequis** : Suivi du module 1 et installation de VMware Workstation

---

## Import des Machines Virtuelles

Les fichiers OVA nécessaires sont disponibles dans le partage réseau `R:\Bundles\ASR2021\M11-Sauvegarde-Restauration-Disponibilité_OVA`. Créez un dossier `D:\VMs` et importez les machines virtuelles suivantes :

| Machine        | Nom du Fichier OVA | Adresse IP              |
|----------------|---------------------|--------------------------|
| Serveur Backup | `srv-backup.ova`    | `192.168.10.2`          |
| NAS            | `truenas.ova`       | `192.168.30.1`          |
| Routeur        | `routeur.ova`       | `192.168.10.254`, `192.168.20.254`, `192.168.30.254` |

Une machine cliente est également à installer avec les options suivantes :
- Windows 10 : `R:\images-virtuelles\vmware\Windows\client\Windows10\W10-*-Base.7z`
- Debian 10 : `R:\images-virtuelles\vmware\Linux\Debian11-cinnamon.7z`

## Tableau Récapitulatif des Machines, Systèmes et Comptes

| Nom        | Type             | Système   | Domaine      | Adresse IP             | Login           | Mot de passe |
|------------|------------------|-----------|--------------|------------------------|-----------------|--------------|
| srv-backup | Windows Server   | 2019      | `enilab.lcl` | `192.168.10.2`         | Administrateur  | Pa$$w0rd     |
| NAS        | FreeBSD - TrueNAS|           | `enilab.lcl` | `192.168.30.1`         | Root            | Pa$$w0rd     |
| Routeur    | FreeBSD - Pfsense|           | `enilab.lcl` | `192.168.10.254`, `192.168.20.254`, `192.168.30.254` | admin | Pa$$w0rd |
| srv-ad1    | Windows Server   | 2019      | `enilab.lcl` | `172.16.x.250`         | Administrateur  | Pa$$w0rd     |
| srv-fic1   | Windows Server   | 2019      | `enilab.lcl` | `172.16.x.1`           | Administrateur  | Pa$$w0rd     |
| ESXi       | VMware ESXi 7    |           |              | `172.16.x.245`         | Root            | Pa$$w0rd     |

*Note : la valeur X du troisième octet de l’adressage est basée sur le dernier octet de l’adresse IP de votre machine hôte.*

---

## Installation des Machines "Physiques" dans Workstation

1. **Récupérez les fichiers OVA** depuis `R:\Bundles\ASR2021\M11-Sauvegarde-Restauration-Disponibilité_OVA`.
2. **Créez une arborescence de stockage** dans `D:\VMs`.
3. **Importez les machines** : `srv-backup.ova`, `truenas.ova`, `routeur.ova`.
4. **Installation d'une machine cliente** : Importez une machine Windows 10 ou Debian 10 préinstallée, configurez la carte réseau en `VMnet12` et assignez une adresse IPv4 libre dans le plan `192.168.20.0/24`.

---

## Installation de l’ESXi et des VMs SRV-AD1 et SRV-FIC1

Référez-vous à la procédure d'installation `ASR2021_M11_Procedure_install_ESXi` pour installer l'ESXi et importer les machines `srv-ad1` et `srv-fic1`.

## Configuration Réseau des Machines Virtuelles

| Machine     | Réseau VMware | Remarques                                         |
|-------------|---------------|---------------------------------------------------|
| ESXi        | VMnet12       | -                                                 |
| srv-ad1     | VMnet ESXi    | -                                                 |
| srv-backup  | VMnet11       | -                                                 |
| srv-fic1    | VMnet ESXi    | -                                                 |
| truenas     | VMnet13       | -                                                 |
| Routeur     | Bridged, VMnet11, VMnet12, VMnet13 | Adresse MAC spécifique à configurer |

---

## Vérification Post-Import

1. **Machines Windows Server 2019** : si le "guest operating system" est configuré sur "other", basculez-le sur "Microsoft Windows" avec la version "Windows Server 2016 ou 2019".
2. **Test réseau** : allumez toutes les VMs et assurez-vous de pouvoir ouvrir une session avec `Administrateur / Pa$$w0rd`.

---

## Vérifications de Connectivité et Intégration AD

- **Depuis `srv-backup`** :
    - Effectuez un ping vers : `srv-ad1`, `srv-fic1`, et `truenas`.
    
- **Préparation du NAS** :
    - Accédez au portail web du NAS via `root / Pa$$w0rd` et exécutez `wbinfo -t` pour vérifier l'intégration AD.
    - En cas de problème, réintégrez le NAS dans le domaine à partir du menu "service d’annuaire" > "Active Directory".
    - Activez le service "ISCSI" sur le NAS.

- **Sur `srv-fic1`** :
    - Connectez-vous à la VM (Administrateur / Pa$$w0rd) et testez la connectivité avec `srv-ad1`, `srv-backup`, et `truenas`.

---

