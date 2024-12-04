# Module 1 : Concepts OSPFv2 à zone unique

## Réseau, Sécurité et Automatisation D'entreprise v7.0 (ENSA)

---

## Objectifs du module

**Titre du module :** Concepts OSPF à zone unique  
**Objectif du module :**  
Expliquer comment le protocole OSPF à zone unique fonctionne sur les réseaux multiaccès point à point et de diffusion.

---

## 1.1 Caractéristiques du protocole OSPF

### Présentation du protocole OSPF

- **OSPF (Open Shortest Path First)** est un protocole de routage à état de liens.  
- Alternative aux protocoles à vecteur de distance comme RIP.  
- **Avantages par rapport à RIP :**  
  - Convergence rapide  
  - Adaptation aux grands réseaux  
- Utilisation de zones pour l'évolutivité.  
- Éléments clés :  
  - Un lien : interface, segment réseau, ou réseau tel qu’un LAN Ethernet.  
  - États de liens : préfixe réseau, longueur du préfixe, coût.

---

### Composants du protocole OSPF

- Échanges d'informations via 5 types de paquets :  
  - **Paquet Hello**  
  - **Paquet DBD (Description de base de données)**  
  - **Paquet LSR (Demande d’état de liens)**  
  - **Paquet LSU (Mise à jour d’état de liens)**  
  - **Paquet LSAck (Accusé de réception d’état de liens)**  
- Utilisation pour détecter les routeurs voisins et échanger des informations.

---

### Bases de données OSPF

- Création et gestion des bases :  
  1. Base de données d’état de liens (LSDB).  
  2. Arborescence SPF via l'algorithme SPF de Dijkstra.  
  3. Table de routage dérivée des meilleures routes.

---

### OSPF à zone unique et zones multiples

- **OSPF à zone unique :**  
  - Tous les routeurs dans une seule zone (zone 0 de préférence).  
- **OSPF à zones multiples :**  
  - Conception hiérarchique.  
  - Réduction des tables de routage, de la charge des mises à jour et des calculs SPF.  

---

### OSPFv3

- Fonctionne comme OSPFv2 mais pour IPv6.  
- Algorithme SPF identique pour les meilleurs chemins.  
- Processus distincts pour IPv4 et IPv6.

---

## 1.2 Paquets OSPF

### Types de paquets OSPF

- Hello, DBD, LSR, LSU, LSAck.

---

### Paquets Hello

- Utilisation pour :  
  - Découverte et établissement des voisins OSPF.  
  - Annonce des paramètres pour la contiguïté.  
  - Sélection des routeurs DR et BDR pour les réseaux multiaccès.

---

## 1.3 Fonctionnement du protocole OSPF

### États de fonctionnement OSPF

- 7 états : Down, Init, Two-Way, ExStart, Exchange, Loading, Full.

---

### Établissement des contiguïtés de voisinage

- Utilisation des paquets Hello pour découvrir et établir des relations de voisinage.  
- Envoi des paquets Hello à l’adresse multicast « Tous les routeurs OSPF » (224.0.0.5).

---

### Synchronisation des bases de données

1. Décision du premier routeur.  
2. Échange des DBD et accusés de réception.  
3. Comparaison des bases de données locales avec LSDB.  

---

### Nécessité d’un DR

- Problèmes des réseaux multiaccès :  
  - Trop de contiguïtés.  
  - Diffusion excessive de LSA.  
- Solution : sélection d’un DR (point de collecte) et d’un BDR (sauvegarde).

---

### Inondation de LSA avec un DR

- DR et BDR réduisent le chaos dans l’échange des LSA.  
- Autres routeurs appelés DROTHER (ni DR ni BDR).

---
