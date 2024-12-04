# OpenIT Cisco3v7 Specimen

## Extracted Content

Découverte réseau avec CDP/LLDP

#

show

 {

cdp 

| 

lldp

}

Affiche la configuration du protocole CDP / LLDP.

(config-if)#

cdp enable

Active le protocole CDP sur l™interface sélectionnée.

#

show cdp interface

Affiche la liste des interfaces CDP actives.

(config-if)#

lldp 

{

transmit 

| 

receive

}

Configure l™interface sélectionnée pour transmettre ou recevoir des paquets LLDP.



(config)#{

cdp 

| 

lldp

} 

run

Active globalement CDP / LLDP sur le périphérique.



(config)#

no 

{

cdp 

| 

lldp

} 

run

Désactive globalement CDP / LLDP sur le périphérique.

#

show 

{

cdp 

| 

lldp

} 

neighbors 

[

detail

]

Collecte des informations détaillées sur les périphériques voisins compatibles 

 

CDP / LLDP.

NTP (Network Time Protocol)

#

clock set 

hh:mm:ss 

{ 

month 

| 

month day 

} 

year

Configure la date et l™heure sur le périphérique.

#

show clock 

[

detail

]

Affiche la date et l™heure configurées localement.

(config)#

ntp server 

ip-address

Configure le périphérique en tant que client du serveur NTP spécifié.

#

show ntp associations

Affiche l™état des associations NTP.

#

show ntp status

Affiche l™état du protocole NTP.

SNMP (Simple Network Management Protocol)

SNMP assure à distance la gestion, la supervision des périphériques réseau ainsi que 



le diagnostic des problèmes matériels et réseau. 

SNMP utilise 3 composants principaux :

-

 

Manager 

(NMS)

 : console d™administration permettant la configuration et le re

-

cueil d™information depuis les nœuds gérés au travers des agents.

-

Nœuds gérés 

: routeurs, commutateurs, serveurs–

-

 

Agents

 : présents sur les nœuds gérés, ils communiquent les données locales

demandées par le NMS et traitent les modifications de configuration qu™il soumet.

SNMPv1 SNMPv2c

SNMPv3

Niveau

noAuthNoPriv noAuthNoPriv noAuthNoPriv authNoPrivauthPriv

1

Authentification Community string Community string Username MD5 / SHA MD5 / SHA

Chiffrement

Aucun

Aucun Aucun Aucun

DES / 3DES 

/ AES

1

image IOS cryptographique requise (k9)

Syslog

Niveau  

de gravité

Nom  

de gravité

Description

0 Urgence Système inutilisable

1 Alerte

Action immédiate requise

2 Critique

Condition critique pour le système

3 Erreur

Condition d'erreur de fonctionnement

4 AvertissementCondition d'avertissement



5 Notification Evènement normal mais important



6 Information Message informatif



7 Débogage Message de débogage

(config)#

service timestamps log datetime

Active l™horodatage des événements consignés. L™heure système doit être préalable

-

ment configurée (manuellement ou via NTP).

(config)#

service sequence-numbers

Active les numéros d™ordre sur les événements consignés pour différencier ceux dis

-

posant d™un horodatage identique.

#

show logging

Affiche la configuration du service de journalisation, ainsi que la liste des évènements 



journalisés.

(config)#

logging console

Configure le service de journalisation pour l™envoi de tous les messages à la console 



pour tous les niveaux de gravité.

(config)#

logging buffered

Configure le service de journalisation pour l™envoi de tous les messages dans une 



mémoire tampon interne pour tous les niveaux de gravité.

(config)#

logging 

ip-address

Configure l™équipement en tant que client du serveur Syslog spécifié.

(config)#

logging trap 

{

level-number 

| 

level-name

}

Limite, en fonction de leur niveau de gravité, les messages destinés au serveur Sys

-

log. Seuls les messag es correspondant à ce niveau de gravité et aux niveaux infé

-

rieurs seront transférés au serveur.

(config)#

logging source-interface 

intf-type intf-number

Active une interface source pour communiquer avec le serveur Syslog.

Cloud IaaS / PaaS / SaaS

IaaS

 : le CSP (

Cloud Service Provider

) fournit à son client l™accès à une machine 

virtuelle (VM), choisie au préalable en fonction de ses capacités hardware/software, 



ainsi qu™à l™ensemble de ses composantes matérielles (vCPU, vRAM, vNIC, vStorage) 



et logicielles (OS, applications). Le client peut ainsi jouir pleinement de cette VM 



(accès et personnalisation de l™OS, installation d™applications–). 

Exemple : location de VM sur Microsoft Azure, Amazon Web Services (AWS)...

PaaS 

: proche du IaaS du point de vue des possibilités matérielles et logicielles 

 

offertes mais dans l™optique de fournir un accès au développeur logiciel à tout un envi

-

ronnement de développement IDE (

Integrated Development Environment

), nécessaire 



à son activité de développeur. 

Exemple : Eclipse IDE, Google App Engine.

SaaS 

: le CSP fournit à son client l™accès à un service clé en main. L™infrastructure vir

-

tuelle fonctionnelle sous-jacente n™est pas exposée au client. Le CSP gère l™ensemble de 

cette infrastructure en arrière-plan (gestion de tout le cycle de vie du matériel, des VM, 



des applications, etc). Exemple : services de messagerie internet (Microsoft 365...), 



stockage Cloud (Dropbox, Google Drive–).

SDN (Software-Defined Networking)

Plan de contrôle 

(

Control Plane

)

Considéré comme le cerveau d™un périphérique, il prend les décisions de transfert 

de couche 2 et 3 et alimente les tables de voisinage, de topologie et de routage IP 



des protocoles de routage, mais aussi les tables ARP ou STP utilisées par le plan de 



données pour acheminer le trafic. Les informations envoyées au plan de contrôle sont 



traitées par le CPU.

Plan de données 

(

Data Plane 

ou

 Forwarding Plane

)

Utilisé pour transmettre les flux de trafic. Les routeurs et les commutateurs utilisent 

les informations traitées par le plan de contrôle pour transmettre le trafic entrant via 

 

l™interface/port de sortie approprié. Les informations du plan de données sont traitées 



par un processeur dédié ASIC (

Application Specific Integrated Circuit

) ainsi qu™une 

 

mémoire rapide TCAM (

Ternary Content Addressable Memory

), sans faire appel au CPU.

Plan de gestion 

(

Management Plane

)

Prend en charge la gestion d™un périphérique via le réseau grâce aux protocoles 

Telnet, SSH, TFTP, SFTP, HTTPS, SNMP, Syslog.

Le contrôleur SDN

 assure de manière centralisée, et à divers degrés d™une solution 



SDN à l™autre, tout ou partie des fonctions du plan de contrôle, tandis que les péri

-



phériques contrôlés gèrent chacun leur plan de données. Le plan de contrôle passe 



infine d™un modèle distribué (sur chaque périphérique) à un modèle totalement ou 



partiellement centralisé (sur le contrôleur uniquement). 

Le plan de données fonctionne cependant toujours sur un modèle distribué.

Solutions SDN et de programmabilité réseau

Solutions SDN

OpenDaylight (ODL) 

Implémentation Cisco :  

Open SDN Controller (OSC)

ACI

1

SDA

2

Propriétaire

ONF

3

Cisco

Cisco

Modèle SDN

Traditionnel 

(Controller-based SDN)

IBN

4

 

(Policy-based SDN)

IBN

4

 

(Policy-based SDN)

Marché

Entreprises (Campus) Data Centers Entreprises (Campus)

Contrôleur

OpenDaylight (ODL) APIC

5

DNA

6

 Center

NBI 

(Northbound Interface)

RESTful

7

 API, Java API RESTful

7

 API

RESTful

7

 API

SBI 



(Southbound Interface)

OpenFlow, NETCONF, 

OVSDB, PCEP, BGP-LS–

OpFlex

Telnet/SSH, SNMP 

NETCONF, RESTCONF

MàJ matérielle et/ou  



logicielle nécessaire

Oui, généralement

Oui

Oui, généralement  

Vérifiez la SDA Compatibility List : 

www.cisco.com/go/sda

Solutions SDN et de programmabilité réseau

Centralisation des fonc -



tions du Control Plane

Oui

Oui, partiellement

Oui

Topologie réseau 

Traditionnelle

Spine & Leaf 

(Fabric Underlay & 

Overlay)

Spine & Leaf 

(Fabric Underlay & Overlay)

1

Application Centric Infrastructure

2

Software-Defined Access

3

Open Networking Foundation

4

Intent-Based Networking

5

Application Policy Infrastructure Controller

6

Digital Network Architecture

7

REpresentational State Transfer

 Outils de gestion de configuration

Les outils de gestion de configuration ont pour objectif commun de réduire la com

-



plexité et le temps consacré à la configuration et à la maintenance des périphé

-

riques d™une infrastructure réseau de moyenne à grande taille.

Ces outils incluent l™automatisation des tâches (telle que la création d™un VLAN ou 

d™une ACL etc.) et l™orchestration qui dicte la manière et l™ordre dans lequel toutes 



ces tâches automatisées doivent se réaliser. 

1

 

déclare dans quel état un périphérique doit finalement être, sans définir les étapes pour y 



arriver à l™outil de gestion de configuration

2

basé sur le résultat attendu, en spécifiant les actions à entreprendre quand une erreur se 

produit

3

sans agent grâce à un Agent Proxy communiquant infine en SSH avec le périphérique cible

4

Domain Specific Language

5

signifie qu™une action aura le même résultat, qu™on l™applique une ou plusieurs fois

OISECAUTCIS.indd   1

OISECAUTCIS.indd   1

08/02/2021   15:40:40

08/02/2021   15:40:40

© Editions ENI - www.editions-eni.fr

© Editions ENI - www.editions-eni.fr

© Editions ENI - www.editions-eni.fr

© Editions ENI - www.editions-eni.fr

© Editions ENI - www.editions-eni.fr

© Editions ENI - www.editions-eni.fr

open

IT

open

IT

open

IT

open

IT

open

IT

open

IT

Qualité de service (QoS)

Trafic Voix

Trafic Vidéo

Trafic de données

Caractéristiques

 

du trafic

- fluide / régulier

- prévisible



- 

 

consommation peu élevée

 

en bande passante 

- 

 

soumis aux contraintes

 

temporelles (délai, retards) 

- 

 

sensible à la perte

 

 

de paquets

- en salves (burst)



- imprévisible



- 

 

consommation élevée

 

 

de bande passante

- 

 

soumis aux contraintes

 

temporelles (délai, retards)

- 

 

sensible à la perte

 

 

de paquets

- fluide / en salves (burst)



- prévisible



- 

 

consommation variable en

 

bande passante

- 

 

non soumis aux contraintes

 

temporelles (délai, retards)

- 

 

insensible à la perte

 

 

de paquets

Latence

200 à 400 ms

non soumis aux contraintes 

temporelles

Gigue

30 à 50 ms

Perte de 



paquets

insensible à la perte  

de paquets

Bande passante

30 à 128 Kbps 384 Kbps à 20+ Mbps

variable

Protocole

Couche 

OSI

Champ utilisé

Utilisation

Codé 

sur

Ethernet 



(802.1Q , 802.1p)

2 Class of Service (CoS)

Trunk 801.1Q

3 bits

Wi-Fi 



(802.11)

2 Wi-Fi Traffic Identifier (TID)

Wi-Fi

3 bits

MPLS

2 Experimental (EXP)

WAN MPLS

3 bits

IPv4 et v6 3 IP Precedence (IPP)

Paquet (de bout en bout)3 bits

IPv4 et v6 3 Differentiated Services Code Point (DSCP)Paquet (de bout en bout)6 bits

 

CS

 (Class Selector) : compatibilité descendante 

avec les valeurs IP P

recedence historiques.

 

AF

 (Assured Forwarding) : 4 classes avec 

des préférences de suppression sélective 



variables en cas de congestion.

 

EF

 (Expedited Forwarding) : file d™attente 

Low Latency Queuing (LLQ) prioritaire pour le 



trafic sensible au délai comme la VoIP.

Routage dynamique OSPFv2

Origine de la route Distance administrative

Route directement connectée

0

Route statique

1

Route résumée EIGRP

5

BGP externe

20

EIGRP interne

90

IGRP

100

OSPF

110

IS-IS

115

RIP

120

EIGRP externe

170

BGP interne

200

(config)#

router ospf

 process-id

Active le routage OSPF avec l™identifiant de processus spécifié et bascule en mode 

de configuration OSPF.

(config-router)#

router-id 

router-id

Définit explicitement un identifiant de routeur OSPF.

#

clear ip ospf process

Réinitialise le processus OSPF en cours d™exécution et donc les contiguïtés de voi

-



sinage OSPF (conseillé suite à la modification de l™ID de routeur ou de la priorité 



d™interface OSPF).

(config-router)#

network 

network-address wildcard-mask 

area 

area-id

Active OSPF sur les interfaces correspondant au réseau spécifié et annonce celui-ci 

dans les mises à jour de routage.

(config-router)#

network

 intf-ip-address 

0.0.0.0 area 

area-id

Active OSPF sur l™interface disposant de l™adresse IP spécifiée et annonce le réseau 

correspondant dans les mises à jour de routage.

(config-if)#

ip ospf 

process-id 

area 

area-id

Active OSPF directement sur l™interface sélectionnée et annonce le réseau correspon

-



dant dans les mises à jour de routage. 

(config-router)#

passive-interface 

intf-type intf-number

Désactive, sur l™interface spécifiée, la formation de contiguïté de voisinage mais 



continue à annoncer le réseau correspondant à celle-ci dans les mises à jour de 



routage.

(config-router)#

passive-interface 

[

default

]

Désactive, sur toutes les interfaces, la formation de contiguïté de voisinage mais 



continue à annoncer les réseaux correspondant dans les mises à jour de routage.

(config-router)#

no passive-interface 

intf-type intf-number

Réactive l™envoi/réception de paquets Hello et donc la formation de contiguïté de 



voisinage, sur l™interface spécifiée.

(config-if)#

ip ospf network {broadcast | point-to-point}

Configure un type de réseau OSPF différent du type par défaut sur l™interface sélec

-

tionnée. Peut servir à désactiver l™élection du DR/BDR sur un réseau point-à-point 



Ethernet.

(config-if)#

ip ospf priority 

value

Définit une valeur de priorité OSPF sur l™interface sélectionnée pour l™élection des DR/



BDR. Une valeur élevée (1-255) augmente la probabilité de devenir DR ou BDR. La 



valeur 0 force le statut DROther.

(config-router)#

auto -cost reference-bandwidth 

{

1000 

| 

10000

}

Modifie la bande passante de référence utilisée dans le calcul de la métrique OSPF 

pour prendre respectivement en charge la bande passante des interfaces Gigabit et 



10 Gigabit Ethernet.

(config-if)#

ip ospf cost 

value

Modifie, sur l™interface sélectionnée, le coût OSPF utilisé dans le calcul de la métrique.

(config-if)#

ip ospf hello-interval 

seconds

Modifie la valeur de l™intervalle 

Hello 

sur l™interface sélectionnée (par défaut 10 sec. 

en Ethernet).

(config-if)#

ip ospf dead-interval 

seconds

Modifie la valeur de l™intervalle temps d™attente 

Hello 

sur l™interface sélectionnée (par 

défaut 40 sec. en Ethernet).



(config)#

ip route 0.0.0.0 0.0.0.0

  {

next-hop-ip

 | 

exit-intf

} 

(config-router)#

default-information originate

Crée une route statique par défaut IPv4 puis la propage dans les annonces de routage 



OSPF.

#

show ip route

 

Affiche la table de routage IPv4 du routeur.



#

show ip protocols

Affiche la configuration du protocole de routage actif.

#

show ip ospf

Affiche les informations OSPF détaillées.

#

show ip ospf interface

 [

intf-type intf-number

] [

brief

]

Affiche une liste détaillée ou résumée de la configuration OSPF de chaque interface 

ou de l™interface spécifiée.

#

show ip ospf neighbor

Affiche les informations relatives aux contiguïtés de voisinage OSPF.

#

show ip ospf database

Affiche le contenu de la LSDB (

Link-State DataBase

) OSPF.

Critères empêchant 2 routeurs OSPFv2 d™établir une contiguïté de voisinage :

 

-

 

Une commande OSPFv2 

network

 est manquante ou mal configurée ;

 

-

 

Une interface sur le lien est incorrectement configurée en tant qu™interface passive ;

 

- Les valeurs des minuteurs OSPFv2 

Hello

 ou 

Dead

 ne correspondent pas ;

 

-

 

Les masqu

es de sous-réseau ne correspondent pas, plaçant ainsi les routeurs sur 

des réseaux séparés ;

 

-

 

 

Les types de réseau OSPFv2 configurés sur les interfaces ne correspondent pas.

Designated & Backup Designated Router

Dans les réseaux à accès multiples uniquement, afin de gérer plus efficacement le 



nombre de contiguïtés et l™inondation de paquets LSA, OSPF élit un 

DR

 et un 

BDR

. 



Le DR est responsable de la collecte et de la distribution des LSA reçus des autres 



routeurs ; il envoie ensuite ces paquets LSA à destination de l™adresse 

224.0.0.5

 (All 

OSPF Routers).

Un BDR est également élu en cas de défaillance du routeur DR. Lorsque le DR n™envoie 

plus de paquets 

Hello

, le BDR s™autoproclame DR et en assume le rôle.

Tous les autres routeurs deviennent 

DROTHER

 (ni DR, ni BDR) ; ils envoient leurs 



paquets LSA aux DR et BDR à destination de l™adresse 

224.0.0.6

 (All DR Routers)

L™élection des DR / BDR est réalisée en fonction de la :

1)

  

Valeur de 

priorité d™interface OSPF 

(comprise entre 0 et 255, 1 par défaut, 0 désac

-

tive la candidature à l™élection)  

 

 

Le routeur disposa

nt de la priorité la plus élevée devient DR, celui dont la priorité 

est la plus élevée après le DR devient BDR.

2)

  

V

aleur de l™

ID de routeur

 

 

 

En cas 

de priorités identiques sur tous les routeurs (cas par défaut), le routeur 

disposant de l™ID de routeur le plus élevé devient DR, celui dont l™ID de routeur est 

le plus élevé après le DR devient BDR.

Listes de contrôle d™accès IPv4

Une liste de contrôle d™accès :

 

- par interface

 

- par protocole (IPv4 ou IPv6)

 

- par direction (IN ou OUT)

/!\ 

Toute ACL dispose d™une ACE implicite 

deny all 

placée en fin d™ACL, qui refusera 

tout trafic non autorisé plus haut dans l™ACL (le traitement des ACL étant séquentiel).



ACL standards :

 

- filtrent les paquets uniquement en fonction de l™adresse IP source du paquet.

 

- utilisent les plages suivantes : 1 à 99 et 1 300 à 1 999.

 

- sont à positionner au plus près possible de la destination à filtrer

.

ACL étendues :

 

- filtrent les paquets IP en fonction : 

Ł

 

des adresses source et destination du paquet

Ł

 

des ports T

CP ou UDP source et destination

Ł

 

du type de protocole (IP

, ICMP, TCP, UDP)

 

- utilisent les plages 100 à 199 et 2 000 à 2 699.

 

- sont à positionner au plus près possible de la source à filtrer

.

(config)#

access-list 

acl-number 

{

deny 

| 

permit 

| 

remark

} {

any 

| 

host 

| 

source

} 

[

wildcard-mask

] [

log

]

Crée une ACL standard numérotée ainsi que son ACE. 

(config)#

access-list 

acl-number 

{

deny 

| 

permit 

| 

remark

} 

protocol source 

[

source-wildcard

] [

operator

 [

port

]] 

destination 

[

destination-wildcard

] [

operator 



[

port

]] [

established

]



Crée une ACL étendue numérotée ainsi que son ACE. 

(config)#

no access-list 

{

acl-number 

| 

acl-name

}

Supprime l™ACL numérotée ou nommée spécifiée.

(config)#

ip access-list 

[

standard 

| 

extended

] 

name

Crée l™ACL standard ou étendue nommée spécifiée et/ou entre dans son contexte. 

(config-std-nacl)#{

deny 

| 

permit 

| 

remark

} {

source 

[

source-wildcard

]} [

log

]

Crée une ACE dans l™ACL nommée précédemment sélectionnée. 



(config-std-nacl)#

sequence-number 

[

permit 

| 

deny 

|  

remark

] {

source 

[

source-wildcard

]} [

log

]

Crée l™ACE avec le numéro d™ordre spécifié dans l™ACL nommée précédemment 

 

sélectionnée.



(config-std-nacl)#

no

 

sequence-number

Supprime l™ACE avec le numéro d™ordre spécifié dans l™ACL nommée précédemment 

sélectionnée.

(config-if)#

ip access-group 

{

acl-number 

| 

acl-name 

} {

in 

| 

out

}

Associe l™ACL spécifiée à l™interface sélectionnée et définit sa direction.

(config-if)#

no ip access-group 

{

acl-number 

| 

acl-name 

}

Désassocie l™ACL spécifiée de l™interface sélectionnée.

(config-line)#

access-class 

acl-number  

{

in 

| 

out

}

Associe l™ACL spécifiée aux terminaux virtuels (VTY) pour filtrer les accès Telnet/SSH.

#

clear access-list counters 

[

acl-number 

| 

acl-name

]

Réinitialise les compteurs des ACL ou de l™ACL spécifiée. 



#

show access-lists

 

Affiche toutes les ACL configurées sur le routeur.



#

show ip interface 

intf-type intf-number

Affiche les éventuelles ACL associées à l™interface spécifiée.

NAT / PAT

Espace d™adressage IP privé (RFC 1918)

Classe PréfixeMasque Plage d'adresses valides

A 10.0.0.0 /8

10.0.0.1 à 10.255.255.254

B 172.16.0.0 /12 172.16.0.1 à 172.31.255.254

C 192.168.0.0 /16 192.168.0.1 à 192.168.255.254

Adresse locale interne 

: adresse privée source vue du LAN, soumise au NAT. 

Adresse globale interne

 : adresse publique source vue du WAN (adresse WAN du 

routeur NAT).

Adresse globale externe

 : adresse publique destination vue du WAN (adresse du 

serveur de destination).

Adresse locale externe

 : adresse publique destination vue du LAN (identique à 

l™adresse globale externe).

Commandes communes à tous les types NAT / PAT

(config-if)#

ip nat 

{

inside 

| 

outside

}



Désigne l™interface sélectionnée comme une interface NAT interne ou externe.

#

show ip nat translations 

[

verbose

]

Affiche les traductions actives présentes dans la table NAT.



#

show ip nat statistics 

Affiche des statistiques et paramètres de configuration NAT.

#

clear ip nat statistics

Efface les statistiques des traductions.

NAT statique

(config)#

ip nat inside source static 

local-ip global-ip



Active le NAT statique en créant un mappage entre une adresse locale interne et une 



globale interne.

NAT dynamique et PAT

(config)#

ip nat pool 

name start-ip end-ip 

{

netmask 

netmask  

| 

prefix-length 

prefix-length

}



Définit un pool d™adresses globales à utiliser pour la traduction NAT dynamique.

(config)#

access-list 

acl-number 

permit 

source 

[

source-wildcard

]

Crée une ACL standa rd identifiant les adresses IP devant être traduites par le NAT 



dynamique / PAT.

(config)#

ip nat inside source list 

{

acl-number 

| 

acl-name

} 

pool 

pool-name

Active le NAT dynamique en liant l™ACL au pool spécifié.

(config)#

ip nat inside source list 

{

acl-number 

| 

acl-name

}  

pool 

pool-name 

overload



Active le PAT en liant l™ACL au pool spécifié.

(config)#

ip nat inside source list 

acl-number 

interface 

intf-type intf-number 

overload

Active la fonctionnalité PAT en reliant l™ACL à l™interface spécifiée.

#

clear ip nat translation *

Efface toutes les entrées dynamiques de la table NAT, conservées 24 heures par 



défaut.

#

clear ip nat translation inside 

global-ip local-ip

 [

outside 

local-ip global-ip

]

Efface de la table NAT l™entrée dynamique spécifiée.

#

clear ip nat translation 

protocol 

inside 

global-ip global-port local-ip local-port 

[

outside 

local-ip local-port global-ip global-port

]



Efface de la table NAT l™entrée dynamique étendue spécifiée.

VPN IPsec

Le Framework IPsec consiste en un ensemble de protocoles permettant le transport 



sécurisé de données sur un réseau IP. Opérant au niveau 3 du modèle OSI, il est en 



mesure de sécuriser tout type de flux IP (contrairement à SSL/TLS qui assure un 



service similaire au niveau 7).

Deux protocoles utilisables seuls ou conjointement assurent la sécurité de la trans

-

mission :

 

-

 

AH

 (Authentication Header) fournit l™authentification et l™intégrité des données, 

mais n™assure pas la confidentialité. 

 

-

 

ESP

 (Encapsulating Security Payload) fournit l™authentification et l™intégrité, mais 

aussi la confidentialité des données.

Suite d™algorithmes courants du Framework IPsec

Type de 

sécurité

Confidentialité

Intégrité Authentification

Algorithme

symétrique

hachage

asymétrique

DES

1

3DES

1

AES

2

SEAL

3

MD5

4

SHA-1

5

SHA-2

5

PSK

6

RSA

7

Tailles de clé

 

disponibles

 

(en bits)

56 3x56 

128 

192 



256

160 128 160

224 



256 



384 



512

512 

1024 



2048

1

Data Encryption Standard

2

Advanced Encryption Standard

3

Software Encryption ALgorithm

 

4

Message Digest

5

Secure Hash Algorithm

6

Pre-Shared Key

7

Rivest Shamir Adleman

La négociation IKE pour l™établissement d™un tunnel VPN IPsec se déroule en 2 phases :

 

-

 

Phase 1 

: les 2 homologues IPsec (pare-feu) s™authentifient soit avec une clé pré-

partagée (PSK), soit avec un certificat, et négocient un profil de chiffrement de 



phase 1 contenant une liste d™algorithmes d™authentification et de chiffrement.

 

 

En cas 

d™échec de l™authentification ou de non concordance des profils de chif

-

frement, la négociation s™arrête. Sinon, un échange chiffré ISAKMP-SA (

Internet 



Security Association Key Management Protocol Œ Security Association

) dans IKEv1 



démarre entre le 2 homologues permettant la négociation de phase 2 chiffrée avec 



la clé de phase 1 ISAKMP-SA.

 

-

 

Phase 2

 : les 2 homologues négocient un profil de chiffrement de phase 2 afin 

que les hôtes expéditeur et destinataire du trafic puissent échanger au travers du 



tunnel VPN IPsec. En cas de non concordance des profils de chiffrement, la phase 



2 échoue. Sinon, pour transmettre les données, 2 canaux sont ouverts (un dans 



chaque direction) utilisant chacun sa propre clé de chiffrement. 

OISECAUTCIS.indd   2

OISECAUTCIS.indd   2

08/02/2021   15:40:41

08/02/2021   15:40:41
