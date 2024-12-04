
# Access Control Lists (ACL)

## Généralités

- Une ACL est une liste de règles permettant de filtrer ou d’autoriser du trafic sur un réseau en fonction de certains critères :
  - IP source, IP destination, port source, port destination, protocole, etc.
- Une ACL permet de soit **autoriser** du trafic (`permit`) ou de le **bloquer** (`deny`).
- Il est possible d’appliquer **au maximum une ACL par interface et par sens** (input/output).
- Une ACL est analysée par l’IOS de manière séquentielle.
  - Dès qu’une règle correspond au trafic, l’action définie est appliquée, le reste de l’ACL n’est pas analysé.
- Par défaut, toute ACL bloque tout trafic non correspondant à une règle explicite.
- Les ACL peuvent aussi servir à **identifier du trafic** pour un traitement particulier :
  - Trafic correspondant à un `permit` est traité.
  - Trafic correspondant à un `deny` est ignoré.

---

## Les ACLs et le Routage

### Types d'ACLs

1. **ACL Standard**
   - Analyse du trafic basé uniquement sur l’**adresse IP source**.
   - À appliquer **proche de la destination** (faible précision).
2. **ACL Étendue**
   - Analyse du trafic en fonction de :
     - Adresse IP source et destination.
     - Protocole (TCP, UDP, ICMP, etc.).
     - Ports source et destination.
   - À appliquer **proche de la source** (grande précision).

---

## Configuration d'une ACL

### Recommandations pour Concevoir une ACL

- Placer les règles les plus précises au début de la liste.
- Les règles les plus génériques doivent être en fin de liste.
- Concevoir une ACL dans un éditeur de texte avant de la configurer par copier-coller.
- Désactiver une ACL sur une interface avant de la modifier.

---

### Exemple d'ACL Standard Numérique

```bash
R1(config)#access-list 1 permit 192.168.0.0 0.0.0.255
R1(config)#access-list 1 deny 192.168.0.0 0.0.3.255
R1(config)#access-list 1 permit any
```

### Exemple d'ACL Standard Nommée

```bash
R1(config)#ip access-list standard monACL
R1(config-std-nacl)#permit 192.168.0.0 0.0.0.255
R1(config-std-nacl)#deny 192.168.0.0 0.0.3.255
R1(config-std-nacl)#permit any
```

---

### Exemple d'ACL Étendue Numérique

```bash
R1(config)#access-list 100 permit tcp any host 192.168.1.100 eq 80
R1(config)#access-list 100 permit icmp 192.168.0.0 0.0.0.255 host 192.168.1.100
```

### Exemple d'ACL Étendue Nommée

```bash
R1(config)#ip access-list extended monACLextended
R1(config-ext-nacl)#permit tcp any host 192.168.1.100 eq 80
R1(config-ext-nacl)#permit icmp 192.168.0.0 0.0.0.255 host 192.168.1.100
```

---

## Vérification des ACLs

### Affichage des ACLs Configurées

```bash
R1#show access-lists
Standard IP access list 1
    10 permit 192.168.0.0, wildcard bits 0.0.0.255
    20 permit 192.168.1.0, wildcard bits 0.0.0.255
    30 deny   192.168.0.0, wildcard bits 0.0.3.255
    40 permit any
```

### Vérification des Matches

```bash
R1#show access-lists workingACL
Extended IP access list workingACL
    10 permit tcp any host 193.190.147.70 eq www (2 matches)
    20 permit icmp any host 193.190.147.70 (14 matches)
    30 deny ip any host 193.190.147.70 (4926 matches)
    40 permit ip any any (878382 matches)
```

---

## Application des ACLs

### Appliquer une ACL à une Interface

- Pour le trafic entrant :
  ```bash
  R1(config-if)#ip access-group 1 in
  ```
- Pour le trafic sortant :
  ```bash
  R1(config-if)#ip access-group 1 out
  ```

### Appliquer une ACL aux Lignes VTY

```bash
R1(config)#line vty 0 4
R1(config-if)#access-class 1 in
```

---

## Suppression d'une ACL

### Supprimer une ACL Numérotée

```bash
R1(config)#no access-list 100
```

### Supprimer une ACL Nommée

```bash
R1(config)#no ip access-list standard monACL
```

---

## Modifier une ACL

1. Entrer en mode de configuration ACL :
   ```bash
   R1(config)#ip access-list standard 1
   ```
2. Supprimer une règle :
   ```bash
   R1(config-std-nacl)#no 20
   ```
3. Ajouter une nouvelle règle :
   ```bash
   R1(config-std-nacl)#15 permit 192.168.1.0 0.0.0.127
   ```

---

## Ressources Utiles

- [Cisco Made Simple](http://www.ciscomadesimple.be)