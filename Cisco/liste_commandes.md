
# Commandes Cisco Complètes avec Explications et Exemples

## **1. Commandes de base pour la navigation**

### `enable`
- **Description** : Passe en mode privilégié (exec).
- **Exemple** :
  ```plaintext
  Switch> enable
  Switch#
  ```

### `configure terminal`
- **Description** : Accède au mode de configuration globale.
- **Exemple** :
  ```plaintext
  Switch# configure terminal
  Enter configuration commands, one per line. End with CNTL/Z.
  Switch(config)#
  ```

---

## **2. Commandes pour les interfaces**

### **Configuration d’une interface IP**
- **Commande** :
  ```plaintext
  interface GigabitEthernet0/1
  ip address 192.168.1.1 255.255.255.0
  no shutdown
  ```
- **Description** :
  - `interface` : Sélection de l'interface.
  - `ip address` : Attribution d'une adresse IP.
  - `no shutdown` : Activation de l'interface.

- **Exemple** :
  ```plaintext
  Switch# configure terminal
  Switch(config)# interface GigabitEthernet0/1
  Switch(config-if)# ip address 192.168.1.1 255.255.255.0
  Switch(config-if)# no shutdown
  ```

### **Afficher les interfaces et leurs statuts**
- **Commande** :
  ```plaintext
  show ip interface brief
  ```
- **Exemple** :
  ```plaintext
  Interface              IP-Address      OK? Method Status                Protocol
  GigabitEthernet0/0     192.168.1.1     YES manual up                    up
  GigabitEthernet0/1     unassigned      YES unset  administratively down down
  ```

---

## **3. Commandes pour VLAN**

### **Création d’un VLAN**
- **Commande** :
  ```plaintext
  vlan 10
  name Sales
  ```
- **Description** :
  - `vlan` : Crée un VLAN.
  - `name` : Donne un nom au VLAN.

- **Exemple** :
  ```plaintext
  Switch# configure terminal
  Switch(config)# vlan 10
  Switch(config-vlan)# name Sales
  ```

### **Assigner un VLAN à un port**
- **Commande** :
  ```plaintext
  interface GigabitEthernet0/2
  switchport mode access
  switchport access vlan 10
  ```
- **Exemple** :
  ```plaintext
  Switch(config)# interface GigabitEthernet0/2
  Switch(config-if)# switchport mode access
  Switch(config-if)# switchport access vlan 10
  ```

---

## **4. Commandes de routage**

### **Route statique**
- **Commande** :
  ```plaintext
  ip route 0.0.0.0 0.0.0.0 192.168.1.254
  ```
- **Description** : Définit une route par défaut (passerelle de secours).

- **Exemple** :
  ```plaintext
  Router(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.254
  ```

### **Routage OSPF**
- **Commande** :
  ```plaintext
  router ospf 1
  network 192.168.1.0 0.0.0.255 area 0
  ```
- **Exemple** :
  ```plaintext
  Router# configure terminal
  Router(config)# router ospf 1
  Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
  ```

---

## **5. Commandes de sécurité**

### **Configurer un mot de passe pour le mode privilégié**
- **Commande** :
  ```plaintext
  enable secret Password123
  ```
- **Exemple** :
  ```plaintext
  Switch(config)# enable secret Password123
  ```

### **Configurer l’accès SSH**
- **Commandes** :
  ```plaintext
  ip domain-name mydomain.com
  crypto key generate rsa
  username admin privilege 15 secret Password123
  line vty 0 4
  transport input ssh
  login local
  ```
- **Exemple** :
  ```plaintext
  Switch(config)# ip domain-name mydomain.com
  Switch(config)# crypto key generate rsa
  The name for the keys will be: Switch.mydomain.com
  How many bits in the modulus [512]: 1024
  % Generating 1024 bit RSA keys, keys will be non-exportable...
  Switch(config)# username admin privilege 15 secret Password123
  Switch(config)# line vty 0 4
  Switch(config-line)# transport input ssh
  Switch(config-line)# login local
  ```

---

## **6. Commandes de sauvegarde et restauration**

### **Sauvegarder la configuration en cours**
- **Commande** :
  ```plaintext
  copy running-config startup-config
  ```
- **Exemple** :
  ```plaintext
  Switch# copy running-config startup-config
  Destination filename [startup-config]? 
  Building configuration...
  [OK]
  ```

### **Restaurer la configuration depuis un serveur TFTP**
- **Commande** :
  ```plaintext
  copy tftp running-config
  ```
- **Exemple** :
  ```plaintext
  Address or name of remote host []? 192.168.1.100
  Source filename []? backup-config
  Destination filename [running-config]? 
  Accessing tftp://192.168.1.100/backup-config...
  ```

---

## **7. Débogage**

### **Activer le débogage OSPF**
- **Commande** :
  ```plaintext
  debug ip ospf events
  ```
- **Arrêter le débogage**
  ```plaintext
  undebug all
  ```
- **Exemple** :
  ```plaintext
  Router# debug ip ospf events
  OSPF events debugging is on
  Router# undebug all
  All possible debugging has been turned off
  ```

---

Ce format Markdown facilite la lecture et l’organisation des commandes avec leurs descriptions et exemples. Si vous souhaitez ajouter d’autres catégories ou approfondir certains sujets, faites-le-moi savoir ! 😊