
# Module 2 : Configuration OSPFv2 à zone unique

## Réseau, Sécurité et Automatisation D'entreprise v7.0 (ENSA)

---

## Objectifs du module

**Titre du module :** Configuration OSPFv2 à zone unique  
**Objectif du module :**  
Mettre en œuvre le protocole OSPFv2 à zone unique sur des réseaux multiaccès, point à point et de diffusion.

---

## 2.1 ID de routeur OSPF

### ID de routeur OSPF

- Un ID de routeur OSPF est une valeur 32 bits unique à chaque routeur dans un domaine OSPF.
- Peut être défini explicitement ou sélectionné automatiquement :
  1. ID configuré manuellement.
  2. Adresse la plus élevée d’une interface de bouclage.
  3. Adresse IPv4 active la plus élevée.

---

### Configurer un ID de routeur

- Exemple : Attribuer 1.1.1.1 comme ID pour R1 :
  ```bash
  R1(config)# router ospf 10
  R1(config-router)# router-id 1.1.1.1
  ```

---

## 2.2 Réseaux point à point OSPF

### Configurer OSPF avec `network`

- Utiliser la commande `network` pour activer OSPF sur des interfaces spécifiques :
  ```bash
  R1(config-router)# network 10.10.1.0 0.0.0.255 area 0
  ```

### Interface passive

- Empêcher la transmission de paquets OSPF sur une interface avec `passive-interface`.

---

## 2.3 Réseaux OSPF à accès multiple

### Routeur désigné (DR) et routeur de secours (BDR)

- DR collecte et distribue les LSA.
- BDR agit en tant que sauvegarde.
- Les autres routeurs sont des DROTHER.

---

## 2.4 Modifier OSPFv2 à zone unique

### Coût OSPF

- Calculé comme :  
  `Coût = bande passante de référence / bande passante de l'interface`

---

## 2.5 Propagation d'une route par défaut

### Configurer une route par défaut

- Commande :
  ```bash
  R2(config)# ip route 0.0.0.0 0.0.0.0 loopback 1
  R2(config-router)# default-information originate
  ```

---

## 2.6 Vérifier OSPFv2

### Commandes utiles

- `show ip protocols`
- `show ip ospf neighbor`
- `show ip ospf interface`