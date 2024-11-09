# Page 1

 
 
 
 
 
Sauv eg arde  

 
Restaur ation 
-
 
Dispon ib ilité
 
S u p p o r t  d e  c o u r s
 
V ersion 
0
9
-
202
4
 
U ne formation, u n diplôme, u n emploi
 
 
ENI 
É
co le Inf orma tique
 


# Page 2

13/09/2024
1
Sauvegarde,restaur ationet 
disponibilité
Form at ion 
Adm inistra teur·tr ice
 
Syst èm eet Réseau
2
Sauv egarde , Restaurat io n, Dispo nibilit é

Mod ule 0 1  

 
Concept, enjeux et définition

Mod ule 0 2  

 
Plan de sauvegar de

Mod ule 0 3  

Type de sauvegar deetim pact resta ura tion

Mod ule 0 4  

 
Sauvegar derdes m achines vir tuelles avecVeeam

Mod ule 0 5  

 
Stockag e 
-
 
réduction de données

Mod ule 0 6  

 
Sauvegar derun ser veurLinux

Mod ule 0 7  

 
La redonda ncede données 

 
RAI D

Mod ule 0 8  

 
La redonda ncede données 

 
Le clustering

Mod ule 0 9  

 
I ntrod uction àla réplication deV M avecVeeam
Ob jectifs
1
2


# Page 3

13/09/2024
2
Mod ule 0 1  

 
Concept, enjeux et définition
Sauvegarde,Restaur ation, 
Disponibilité
4
Sauv egarde , Restaurat io n, Dispo nibilit é

Co n cept & en jeu x 

Bon nes pratiques

Sau vegardeet archivage

Restau ra tio n

Dispo n ibilité 

Règle 3
-
2
-
1

PCA / PRA / Plan de sau vegarde
Concept, Enjeux, définition
3
4


# Page 4

13/09/2024
3
5
Co ncept et enje ux
Con cept


gar an tirla péren n itédes do n n ées

assu rer la récup éra tio n  desinfo rmat ion s ind ispen sab les au  
 


répo n dreau x deman desdedispo n ibilité des do n n ées
S auvegarde, Rest auration, Disponibilité
6
Co ncept et enje ux
Enjeux

Préven ir la per te dedo n n ées

Avo ir u n plan  desecou r s en cas de défaillan ce matérielle o u log icielle

G ar an tirla réten tio n  desdo n n ées réglemen taires

Avo ir u n epro tectio n con treles cyberatt aqu es

Préven ir l'in tr u sion , l'in cen die .. .
S auvegarde, Rest auration, Disponibilité
5
6


# Page 5

13/09/2024
4
7
Sauv egarde , Restaurat io n, Dispo nibilit é
Bo nn es pr at iques

Créer
 
u n compte dédié à la sau vegardesu r vo treA D :


à sau vegarder

en cas depro blème, il pro cureu n emeilleu re tr açabilité dan sles log s

Po u r les clien ts Wind o ws, u tiliser le gro u pe 
opérateurde sauvegar de 
qui permetdesauvegarder etrestau rerdes fichier s sans condition  
d'accès au x fichier s en  lectu re o u écritu re.

Ren seign er et gén érer un  plan de sau vegarde.
Co ncept et enje ux
8
Défi niti o n / C o ncept
S auvegar deet Ar chivage
Ne pascon fon dreces deux n o tio n s : 
Sauvegar de
 
Sauvegar de:
Opération  qui consiste à dup liquer età conser ver demanière sécurisée 

au trequ ecelui qu i les con tien t actu ellemen t afin  d'en assu rer et d'en  
gar an tirla

man ipu lation  po r tan t atteinte àleu r intégr ité.
S auvegarde, Rest auration, Disponibilité
7
8


# Page 6

13/09/2024
5
9
Défi niti o n / C o ncept
S auvegar deet Ar chivage
Ne pascon fon dreces deux n o tio n s : 
Sauvegar de
 
Archivag e :

Pro cessu s qu i gèrela con ser vatio n  des do n n éesdepro du ctio n , 
ap plicatives o u systèmes po u r desra iso n s jur idiques, fiscales, 
administr atives, so ciales o u o pératio n n elles.

La con ser vatio n
des équ ipemen ts log iciels et matériels n écessaires à 
la bo n n eexp loitat ion
des archives fait égalemen t par tie du périmètre 
de l'archivage
S auvegarde, Rest auration, Disponibilité
10
Défi niti o n / C o ncept
Rest aur ati on(déf i ni ti onW i ki p édi a)
La"rest aurat iond ed onnées " ou "récupérat iond ed onnées " est une 
opérat ion
q uicons isteà 
retrouverles do nnéesp erdues 
à la suited 'une 
erreur hum aine,uned éfaillance m atérielle,unaccident ouau m oment  
oppor t un d 'untest d erécupérat ion d ed onnées d éfini d ansuneprocédured e 
s t ratégied e
s auvega rd e
et d 'archive
(éga lem ent appelé 
p lande sauvega rde
). 
Lad ifficulté d elarest aurat iond ed onnées varie beaucoup, pouvant êtreune 
s impleform alitéou, aucont raire, und éfitechnologiq ue. 
Des
log iciels
s pécifiq ues exis tent et plus ieur s ent reprises ses pécialisent d ans 
led omaine.
S auvegarde, Rest auration, Disponibilité
9
10


# Page 7

13/09/2024
6
11
Défi niti o n / C o ncept
Disp o nib ilité
 
 
la dispo n ibilité du SI
 
s'exp rime 
en  po u rcen tag e 
:
Disp o nib ilité
 
= MT BF/ (MTBF+MT T R)
MT BF
 
(
Me an
 
T ime  
Betwe en
 
Failure
) : mesu redu temps estimé en tre2 

MT T R
 
(
Me an
 
T ime to 
Reso lutio n
): mesu redu temps estimé po u r 
 
S auvegarde, Rest auration, Disponibilité
12
Défi niti o n / C o ncept
S auvegarde, Rest auration, Disponibilité
D isponibilité en p ourcentag e
11
12


# Page 8

13/09/2024
7
13
So lut io ns clo ud
Défi niti o n / C o ncept
Tro i s
co pi es de do nnées  
: 

et au minimum deux sauv egardes.
Deux
ty pes  de s to ckage di ff érents  
: 
Deux co pies des do nnées sauv egardées do ivent être co nser vées sur deux 
suppo r ts de sto ckage distincts. Cela permet de minimiser les risques de 
défaillance qui po urr aient po tentielleme nt sur venir sur un suppo r t unique. 
Exemples de types de stockage : disque dur interne, disque dur externe,  bande 
magnétique, clé USB  o u enco re une sauv egarde dans le clo ud.
Une
 
co pi e ho rs  s i te:
 
il est impératif de co nser ver au mo ins une co pie des 
 
incendie, tempête, co ur t
-



co pies.
Règle 3
-
2
-
1
14
Défi niti o n / C o ncept
P CA ,P R A
PCA : Plan d e Continuité d ' Ac tiv i té
Regroupe tous les processus  mis en plac e avant  et après une 
sit uat ion d e cr ise, il conc erne :

Lerétablissement dusy stèmed'info rmation

La gestion de la communication interne et externe

Lerepliphy siquedes utilisateur s

La gestion de la sécurité et desrisques sanitaires

La gouvernancede la gestion de crise
S auvegarde, Rest auration, Disponibilité
13
14


# Page 9

13/09/2024
8
15
Défi niti o n / C o ncept
P CA , P RA
PRA : Pla n de  Rep rise d'Activité
Reg ro u p el'en semb le d es p ro céd u reset mo yen s
n écessaires à la 
co n tin u ité d u système d 'in for mat io n , il co mp ren d :

La politique ou plande sauvegarde

La gestion dustocka ge deséléments nécessairesà la restauration

La procédurede restaurationdusy stèmeet desdonnées

Leslicences des diff érentesapplication utilisées
Le 
plan de repr ised'activité 
n'est 
qu'une des com posantes 
du  
plan de  continuité d'a ctivité.
S auvegarde, Rest auration, Disponibilité
16
Sauv egarde , Restaurat io n, Dispo nibilit é
Mis een placede l'enviro nnement
TP1
Démo
15
16


# Page 10

13/09/2024
9
Mod ule 0 2  

 
Le plan de sauvegar de
Sauvegarde,Restaur ation, 
Disponibilité
18
Sauv egarde , Restaurat io n, Dispo nibilit é

P landes a uvegarde

Périmètre
de sa uvegarde

Périmètre 


N iveaudecriticitédesdo nnées

Lato léra ncea uxper tes

Fenêtre, fréquenceetpério dicité

Editeurdes o lutio nsdes a uvegarde

VE RI TA SBacku p E xec

VE E A MBacku p &Réplicatio n
Le Plan deSauvegar de
17
18


# Page 11

13/09/2024
10
19
Pl a n de s a uvega rde
Le plan de sauvegar de
Leplan desauvegarde estune 
pr océd u r e
 
qui détaille les 
donn ée s
 
info rmatiques qui doivent êtresauvegardées,l'
infr a str u cture
 
de sauvegarde, 
le 
ca len dr ier  
des copiesà réaliseret les 
mét hode s
 
de récupération et 
restauration.
Il intègre 
a min ima  
les élémentssuivants :

Lepérimètre(liste des ressourcesà sauvegarder)

Les contraintes

Lesdiff érents ty pesde sauvegarde

La fréquence/périodicité des sauvegardes

Lesinfo rmations destocka ge

Lesprocéduresde test de restauration

La destruction des suppor tsay antcontenu les sauvegardes
S auvegarde, Rest auration, Disponibilité
20
Pl a n de s a uvega rde
Le pér im ètrede sauvegar de=quelles données sa uvegar der?
Identifier le périmètre passe par un inventaire des éléments à sauv egarder :

Documents / F ichier s

B ases de do nnées



A pp licatio ns, co urr iels, etc.
S auvegarde, Rest auration, Disponibilité
19
20


# Page 12

13/09/2024
11
21
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Le pér im ètredu syst èm ed'inform at ion

Les ap plicatio n s 
 

Les ser veu r s/
l'
en viro n n emen t réseau

Les po stes detr avail info rmat iqu e 
(fixes o u no mades)

To u tes les info rmat ion s déten u es par l'en trepr ise 
(co urr iels,
 
22
Pl a n de s a uvega rde
Niveau de criticité desdonnées

en cas
d'in dispo n ibilité.
Le classemen t de criticité est basé su r deu x car actéristiqu es :

La sensibilité de l'info rmation 
: co nfidentiel, unique et difficile à reco nstituer en 
o pp o sition aux info rmations de ro utine, de co nfo r t.

La dispo nibilité de l'info rmation
 
: f réquence et urgence d'accès.
S auvegarde, Rest auration, Disponibilité
M atr ice  de de g ré de  cr iticité
DI SPO NI BILIT E
FAIB L E
MOY E NNE
FO RT E
SENSI BILIT E
FAIB L E
1
1
2
MOY E NNE
2
2
3
FO RT E
3
3
3
21
22


# Page 13

13/09/2024
12
23
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Latoléra nce a ux per tes
PDM A (P
erte d e 
D
on n ées 
M
aximale 
A
d missible) /
RPO (
R
ecovery
 
P
oint 
O
b jective)
Qua nt if ielesd on n ée sq u 'u n système d 'infor mat ionp eu t êt reame n éàp erd re 
su iteà u n in cid ent .Elle cor resp on d
à lad u rée e
vı „o[]v ]ˆ ˚vı› „}À}‰ µ vı
p er ted ed on n ée set lad atelap lu srécented esd on n ée sq u iserontu t ilisée s 
en remp laceme nt d esd on n ée sp erd u es. 
24
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Latoléra nce a ux pannes
DM IA (D
u rée 
M
aximale d '
I
nterru p tio n  
A
d missib le) / 
RTO (
R
eco very
 
T
ime
 
O
b jective)
Con st it u eletemp smaximalaccep tab led u rant leq u elu n eresso u rcep eu t n ep as 
êt red isp on ib leap rèsu n einter ru p t ion d u ser vice.
D an sle cad red elasau vegard ecela  cor resp on d au temp smaximalaccep téd e 
restau rat iond esd on n ée s.
23
24


# Page 14

13/09/2024
13
25
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Fenêtre de sauvegar de
Désign e la 
plagede temps
 
du ra n tlaqu elle le 
pro cessu sde sau vegarde
 
se 
déro u le:

Défin ir q u an d les 
accès
 
u tilisateu r s et applicatifs so n t les plu s 
re stre ints
 
: n u it, week
-
en d. ..

Lim iter
 
au maximum l'
im pact
 
deper for man cedes ser veu r s et du 
réseau .
26
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Fréquence ou périodicité de sauvegar de
Défin ie en  fon ctio n de plu sieu r s par amètresliés au con texte del'en trepr ise 
o u au x élémen ts su ivan ts :

La to léra n ce au x per tes en cas de sinistre (PDMA )

Le vo lume dedo n n éesà sau vegarder

La vitesse d'évo lut ion  des do n n ées

Le coû t en gend répar le pro cessu s desau vegarde
25
26


# Page 15

13/09/2024
14
27
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
D urée derétention desdonnées
Cer taines do nnées o nt une durée légale de co nser vatio n : les sauv egardes 
permettent
de garantir cette rétention,
cela viendr a
questio nner le cho ix 
des
suppo r ts de sto ckage.
3  a ns

Factures c lients

Com ptes annuels

Factures fourniss eur s

Livre c om m erc eet annexes

D éc laration endouane
5  a ns



D oc um entsbanc aires

Registres deproc ès
-
verbaux

Vérification /c ontrôle du CSE

Bulletin de paie

D os sier sAc c idents du travail
1 0  a ns

Livre et registre c om ptable

 

Co ntrat co nc lu par vo ie élec tro nique avec  
un co nso mmateur

Com pte annuel
3 0  a ns



Pièc e c onstitutives de laso c iété

Correspondanc e c om m erc iale

Registre desdélégués duper so nnels
28
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Editeur sde so lut ion s de sauvegar de
Les éditeu r sde so lut ion s de sau vegardeso n t no mbreu x su r le marché 
avec des solu tion s gratu ites ou payantes.
AT E MPO
T ime Navigato r
ARCSE RV E
Unified
Data Pro tec tio n
CO H ESIT  
DataP latefo rm
CO MMVAULT  co mplete Ba c kup & reco very
DE L L  E MCData Pro tec tio n Suite
BE E MO  
BeeH ive
U˚˚u } o}µˆUo]v˚Y
SPECT R UMPro tec t
R UBR IKClo ud Data Managem ent
STO R AGECR AFT  O neXafe / Shado w Xafe
V E EAMBa c kup and Réplicatio n
Ve r itas 
Netbackup
/ 
Backup E xe c 
(solution 
utilisé e
pour  la suite  du module )
27
28


# Page 16

13/09/2024
15
29
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Présenta tion :Verita s Backup 
Exec
O nglets
Bo uto n B ac kup 
E xec
R uban co mmandes
Vo let de sélec tio n
Vo let d' info rmatio ns
 „„˚[ıı
Bac kup 
Exec
est un lo giciel de
sauv egarde
et
restauration de do nnées
édité par 
la société
Veritas. Il fo urnit des fo nctionnalités de sauv egarde et d'archivage.
Gestio n des 
travaux
30
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Présenta tion :Verita s Backup
Exec
O n gl ets :

Accu eil.Off reu n accès rap id eau xinfor mat ion sd eBacku p  
Exec
 

Sau vegard eet restau rat ion .Créez u n t ravaild esau vegard eou d e 
restau rat ion.

M on iteu rd est ravau x.Su r veillez et gérez les op érat ion s.

Stockage.Configu rez le stockage,exécu tez d esop érat ion sd estockageet  
gérez lesméd ias.

Rap p or t s.Rap p or t srelat ifsau ser veu rBacku p  
Exec
Ru b an d e co mman d e
Contie nt lescom man d esd 'act ion sq u ivarie nt en fon ct ion d ech aq u eon glet .
Vol et d e sélect i on
Sé lect ion n ez lesélé mentsavec lesq u elsvou ssou h aitez t ravailler.
29
30


# Page 17

13/09/2024
16
31
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
G esti on d es Travau x
Per met d 'accéd er àla gest ion d etou teslesop érat ion sp ou rleser veu r 
séle ct ion n é.
Vol et Détai l s
Les d étailssup p lémentairess'aff ich ent p ou rleser veu r sélect ion n é.
Bar red 'état
Fou rn it d esinfor mat ion sau su jet d u ser veu rBacku p  
Exec
, d est ravau xq u isont  
en cou rsd 'exécu t ion ou sont p lan if iés,d esale rteset d esser vices.
A ct u al i ser
Cliq u ez su r
F5
p ou rréa ct u aliserl'inter faceu t ilisateu rd ela con sole  
d 'ad min ist rat ion .
Présenta tion :Verita s Backup 
Exec
32
Pl a n de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Etape pourla sauvegar ded'un ser veur :
1.
Ajout d'un m ag asinde stockag e

Onglet "Stockage"
 
==>
 
"con figurer le stockage"

Valider l'assistan t en fon ctio n  du type de sto ckag eso u h aité
2.
Ajout du ser veurà sauvegar der

On glet "sau vegardeet restau ra tio n" 

Clic dro itdan s l'espace vide du "vo let de sélectio n" ==> "ajo u ter 
u n ser veu r"

Valider l'assistan t en fon ctio n  du type du ser veu r cible
3.
Mise en place du job de sauvegar de
1.
On glet "sau vegardeet restau ra tio n"=>
"Sau vegarder" 
2.
Valider l'assistan t en fon ctio n  du type de sau vegardeà réaliser
Présenta tion :Verita s Backup 
Exec
31
32


# Page 18

13/09/2024
17
33
Sauv egarde , Restaurat io n, Dispo nibilit é
Inst a lla tio net co nfigura tionde
Verita s Ba ckup
-
Exec
Démo
TP2
Mod ule 0 3  

Type de sauvegar deetim pact de la resta ura tion
Sauvegarde,Restaur ation, 
Disponibilité
33
34


# Page 19

13/09/2024
18
35
Sauv egarde , Restaurat io n, Dispo nibilit é

Ra pp el3.2.1

Rot at iondessuppo r ts etSys tèmeGP F

Sauvegardeà chaud, à f ro id



Co mp lète,incrémenta l,diff érentielle

Rest a ura tion
Type de s auvegarde et i mpact restauration
36
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Tro i s
co pi es de do nnées  
: 

et au minimum deux sauv egardes.
Deux
ty pes  de s to ckage di ff érents  
: 
Deux co pies des do nnées sauv egardées do ivent être co nser vées sur deux 
suppo r ts de sto ckage distincts. Cela permet de minimiser les risques de 
défaillance qui po urr aient po tentielleme nt sur venir sur un suppo r t unique. 
Exemples de types de sto ckage : d isque dur  interne, disque dur  externe,  bande 
magnétique, clé USB  o u enco re une sauv egarde dans le clo ud.
Une
 
co pi e ho rs  s i te:
 
il est impératif de co nser ver au mo ins une co pie des 
 
incendie, tempête, co ur t
-



co pies.
R
ap p el : Règle 3
-
2
-
1
35
36


# Page 20

13/09/2024
19
37
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Tro i s
co pi es de do nnées  
: 

et au minimum deux sauvegardes.
Deux
ty pes  de s to ckage di ff érents  
: 
Deux co pies des do nnées sauv egardées do ivent être co nser vées sur deux 
suppo r ts de sto ckage distincts. 
Une
 
co pi e ho rs  s i te:
 
u n e co p ie sto ckée d an s le clou d  o u su r u n au tre site
Ext ension
 
: Règle 3
-
2
-
1
-
1
Une
 
co pi e ho rs  l i gne :
 
une 
} › ]˚ ’ı} l˚ ’v ’ o]˚v µ’˚µ ˆ ˚˚vı„˚› „]’˚U › „} ıP˚v ]v ’ ˆ ˚’
cy b erattaq u es
x  1
38
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
La vision  VEE AM: Règle 3
-
2
-
1
-
1
-
0
Aj o ut de l a notio n 
Zéro  
Erreurs
37
38


# Page 21

13/09/2024
20
39
Ty pe de s a uvega rde
S auvegarde, Rest auration, Disponibilité
Ro t at ion des sup p o r t sdesauvegar de

Scénar io desauvegar detra ditionnel 
GPF
 
(Gr a nd
-
père/Père/Fils)

En a nglais :  
GFS
 
(G ra nd
-
fa th e r
/
F a th e r
/ Son).

La ro tat ion G ra n d
-
père/Père/Fils est la plan ificatio n  dero tat ion des 
médias la plu s cou ra mmen t utilisée :

Supp o r t quo tidien 

 
F ils

Supp o r t hebd o madaire  

 
Père

Supp o r t mensuel  

 
Grand
-
Père

U n estr atégie de ro tat ion  
GFS
 
su r 5 jo u r s n écessite en viro n  
21
ban despar an .

U
n estr atégie su r 7 jou r sn écessite en viro n 23
ban despar an  (deu x 
ban desqu o tidien n es deplu s). 

Po ur ces deux planificatio ns, le no mbre de médias nécessaires varie selo n les 
critères de co nser vatio n spécifiés et le no mbre de do nnées sauv egardées. 
41
Ty pe de S a uvega rde
Sauveg ard e, Restaurati o n, Disp o ni b i li té
Ro t at iondes sup po r t sde sauvegarde
Rotati on stan d ard avec G FSsu r 5j ou rs(21 b an d es)
Ba ndes Fils  Quo tidienne 
( 4 jo urs puis rec yc lées
)
Ba ndes Père  H ebdo madaire 
( 5 semaines puis rec yc lées
)
Ba ndes Grand
-
Père  Mensuelles
( 12 mo is puis rec yc lées
)
1
2
3
4
5
8
1
2
3
4
Semaine 1
6
1
2
3
4
7
1
2
3
4
1
2
3
4
9
1
2
3
4
10
1
2
3
4
5
1
2
3
4
11
12
13
14
15
16
17
18
19
20
21
Semaine 2
Semaine 3
Semaine 4
Sem aine 5
Semaine 6
Semaine 7
Semaine 8
39
41


# Page 22

13/09/2024
21
42
Ty pe de s a uvega rde
Sauveg ard e, Restaurati o n, Disp o ni b i li té
Sauvegar deà
chaud
Les do n n éesso n t sau vegardées en même temps qu'elles so n t utilisées 
par l'ut ilisateu r
:
+
Im médiatement accessibles
+
Facilem ent m odifiables
-

S auvegar deà chaud età fr o id
Lo r sdu pro cessu s de sau vegarde, les do n n éespeu ven t êtreaccessibles au x 
u tilisateu r s
o u n o n . 
43
Ty pe de s a uvega rde
Sauveg ard e, Restaurati o n, Disp o ni b i li té
SauvegardeàFroid
L'u tilisateu r n'apasaccès au x don n éesdu ra n t to u t le pro cessu s de 
sau vegarde:

+Facile à
resta urer
-
I nterr uption du ser vice le tem psde la sauvegar de
S auvegar deà chaud età fr o id
Lo r sdu pro cessu s de sau vegarde, les do n n éespeu ven t êtreaccessibles au x 
u tilisateu r s
o u n o n . 
42
43


# Page 23

13/09/2024
22
44
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodes desauvegar des 
I l existe plu sieu r s méth o desde sau vegarde, ch acu n e des méth o des 
définies ci
-
ap rès fon ctio n n e avec des att ribu tsde fichier s spécifiqu es, 
 
Systèmede Da te
Beau cou p plu s simple qu ele bit d'archivage, u n ecompar aiso n  est 
réalisée en trela datede créatio n , o u  demo dificatio n , et la datede la 
dern ièresau vegarde.
45
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodes desauvegar des 
Attr ibut d'archive : Le bit d 'ar chivag e
Fich ier
o rigine
Bit a rch ive = 0
Fich ier
N +1
Bit a rch ive = 1
Créatio n
-
Mo dificatio n
fermeture
Fich ier
N +1
Bit a rch ive = 0
sauvegarde
44
45


# Page 24

13/09/2024
23
46
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Mét ho des desau vegar des 
Sa uveg a rd eCom plète
Co p ie l'en semb le d es fich ier s et
do ssier s
d'u n système : impact
su r
le 
sto ckag e
impo r tan t.
Sa uveg a rd e
I ncrém enta le
L'in crémen tale
effectu e
d'ab o rd
u n epremière
cop ie
complète
et ch aqu e 
sau veg ard esu ivan te p ren d ra
en  compteles mo dificatio n s 
ap p o r tées
depu is la sau vegarde précédente(co mplète
o u différen tielle).
Sa uveg a rd eD iffér entielle
La d ifféren tielle
effectu e
d'ab o rd
u n epremière
cop ie
complète
et ch aqu e 
sau veg ard esu ivan te p ren d ra
en  compteles mo dificatio n s 
ap p o r tées
depu is la dern ière sau vegarde
Co mplète.
47
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodede sauvegar des 
Sauvegar deCom plète
Sau vegard elatotalitéd esf ich iers,mo d if iésou n on .Elle est la b ased etou te 
solu t ion d esau vegard e.
Fon ct i on n ement:

Ne
seb asep assu rl'att rib u t p ou rsavoir  q u oisau vegard er,elle sau vegard etou t !

M od if ie
l'att rib u ten f in d esau vegard ep ou rmarq u er lef ich ier.
lun
mar
m er
jeu
ven
Sauvegarde co mplète
46
47


# Page 25

13/09/2024
24
48
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodes desauvegar des 
Sauvegar deCom plète
Avantage :

Restau rat ion
rap id eet simp le

Sau vegard e
lap lu sf iab le

Per met
d esu p p rime rt rèsfacileme nt les an cien n essau vegard es
I n co nvén i ents :

Trèsgou rma n d en esp aced estockage sil'on sou h aite
gard er les 
an cien n es
sau vegard es

Les f ich iersq u in 'ont p asétémo d if iésserontsau vegard és
p lu sieu rsfois
49
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodes desauvegar des 
SauvegardeIncrémentale
La sau vegardeincrémen tale, sau vegarde
les do n n éesmo difiées 
o u ajo u tées depu is la dern ière sau vegardecomplète pu is 
incrémen tale.
Fonctionnem ent :

Pren d to u s les fichier s ayan t leu r satt ribu ts A rchiveà 1

A prèsla
sau vegarde
l'attr ibu t
est
remis à0.
lun
mar
mer
jeu
ven
Sauvegarde co mplète
Fic hiers
 
c rées o u mo difiés
48
49


# Page 26

13/09/2024
25
50
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe
 
de s a uvega rde
Méthodes desauvegar des 
Sauvegar deI ncrém enta le
Avantage :

L'espace
desto ckag e

Le
tempsde sau vegarde

La con so mmation
de la ban depassan te
I nconvénients:

Temps

Co mplexité et fiab ilité dela restau ra tio n des do n n ées
51
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe
 
de s a uvega rde
Méthodes desauvegar des 
Sauvegar deD ifférentielle 
-
 
cum ulat ive ou T 1
Sau vegarde
les do n n éesmo difiées o u ajo u tées
depu is la dern ière 
sau vegardecomplète ap pelée "Base différen tielle".
Fonctionnem ent :

Pren d to u s les fichier s ayan t leu r attr ibu t A rchiveà 1.

A prèsla sau vegardel'attr ibu t
n'est pas remis à0,  méth o dedite 
cumu lative.
lun
mar
mer
jeu
ven
Sauvegarde co mplète
Sauvegarde différentielle : 
Fic hiers
 
c réés o u mo difiés
50
51


# Page 27

13/09/2024
26
52
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodes desauvegar des 
Sauvegar deD ifférentielle 
-
 
cum ulat ive ou T 1
Avantage :

Restau ra tio n  simple et ra pide

Temps de sau vegardemo déré

Plus fiab le
qu'u n esau vegarde 
incrémen tielle
I nconvénients:

Plus len te et cou teu se qu'u n esau vegarde incrémen tielle

Pas deréman en ce su r les fichier s si u n seu l su pp o r t desau vegarde est 
u tilisé
53
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodes desauvegar des 
SauvegardeIncrémentielle Inver sée
E lle se base su r un eincrémen tielle, mais va con str u ire u n esau vegarde 
complète cha qu e jou r (o u  àcha qu e o ccu rren ce)
Fonctionnem ent :

Sau vegardeen  mo deincrémen tielle 

les do n n ées so n t en su ite fusion n ées avec la sau vegarde an térieu re 

Cela crée u n esau vegarde complète «
recon str u ite
».
lun
mar
mer
jeu
ven
Sauvegarde co mplète
Fic hiers
 
c rées o u mo difiés
52
53


# Page 28

13/09/2024
27
54
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe
 
de s a uvega rde
Méthodes desauvegar des 
Sauvegar deI ncrém entielle I nver sée
Avantage :


complète

Co n so mmation de sto ckag eiden tiqu e à celle 
du mo de 
incrément ielle

La con so mmation
de la ban depassan te
I nconvénients:

Temps et resso u rcesmachin es su pp lémen taires po u r la fusion  
des sau vegardes
55
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Méthodes desauvegar des 
:
synt hèse
Méthodede 
sau vegar de
Don n éessau vegar dées
Temp sde 
sau vegar de
Temp sde 
r estau r ation
E spacedisqu e 
occu p é
Atou ts
Limites
S auvegarde 
com plète
Toutes
L ent
Rapide
Élevé
F iabilité
Espacede 
stockage 
im por t ant
S auvegarde 
incrém ent ale
Uniquem ent les données 
m odifiéesparrappor t  àla 
précédentesauvegarde
Rapide
Modéré/long
L eplusfaible
Volum ede 
sauvegarde 
réduit
Nécessite 
toutesles 
sauvegardes
S auvegarde 
différent ielle
Uniquem ent les 
données
m odifiéesdepuis 
la
précédentesauvegarde 
com plète
Modéré
Rapide
Modéré
Rest aurationà 
par t ir dela 
dernière 
sauvegarde
S auvegarde 
volum ineuse
S auvegarde 
incrém ent ielle 
inversée
Toutes 
(fusiondesdonnéesde 

com plèteprécédente)
Modéré
Rapide
P lusfaible
Unesauvegarde 
com plèteau 
plusprochedes 
donnéesde 
product ion
Per form ance 
supplém ent aire 
pour 
reconst ruireles 
backupsfull.
54
55


# Page 29

13/09/2024
28
56
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Rest aur at ion
La restau ra tio n d'élémen ts, qu e ce so it u n fichier, u n eap plicatio n , u n e 
basede do n n ées, o u u n système complet est la fin alité de to u splan  de 
sau vegarde.
On  n'ajamais dep r o b lèmedesauvegar de, 
que des p r o b lèmesde r est aur at ion !
Les sau vegardesqu e l'on réalise do iven t 
OBLI GATOI REMENT  ÊTRE 
T EST ÉE 
à inter valle régu lier.
U n plan  desau vegarde n esera  con sidéré comme complet qu'ap rèsavo ir 
effectu é ces tests.
57
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Rest aur at ion
Laresta ura tionà la dem ande
Co n cern edes fichier s perdu s, effacés o u  altérés. Plusieu r s po ssibilités 
so n t dispo n ibles :

Restau rer
su r l'or iginal (risqu e deper te desdo n n ées actu elles)

Restaurersur un em placem ent différent
 
du  mêmesystème

Pro tection co ntre l'écraseme nt

Le plus co uramment utilisé

Restau rer su r u n au tresystème

Co ntrô le avant reto ur en pro ductio n

Palier des pro blèmes de sto ckage

Restauration co mplète de machines vir tuelles

Restau rer un ean cien n e ver sion  via le 
ver sionning
56
57


# Page 30

13/09/2024
29
58
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Rest aur at ion
Laresta ura tiond'une basede données
v ŒÇ›ˆ„˜Po˚Z ‰ µı Ç›˚ˆˆ ]’› }’˚ˆ [µ v}µ› oµ ’]˚µ „
mét h od esd erestau rat ionq u ilu iest p rop re.Exemp les:

Base SQL Ser ver => restau ra tio n via SQL 
Ser ver Ma n agemen t Stu dio

Base 
Mysql
 
=> restau ra tio n via l'impo r t
d'u n fichier 
DUM P.sql

m ysql
--
user=
m on_user
--
pass word
=
m on_pass word
< 
fichier_so urc e.sql

Base Ora cle =>
restau ra tio n des fichier s depu is u n esau vegardeà 
fro id ; impo r t 
dat ap u mp
 
; u tilisatio n  deRM A N. ..
59
Sauv egarde , Restaurat io n, Dispo nibilit é
Ty pe de s a uvega rde
Rest aur at ion
Laresta ura tiondu syst èm ed'exploita tion com plet d'un ser veur
Les solu t ion su t ilisant u n emét h od eap p elé e 
Bare
-
M etal
-
Recover y
 
p er mettent  
„˚}v ’ı „µ ı ]}vˆ [µ v’Ç’ı˜u˚}u › o˚ı › „ıˆ [µ vv }µ À˚oo˚µ v ]ıˆ 
d isq u es.
Co n d i ti on set étap es
1 
t
 
„Z ]ı˚ı µ „]]ˆ ˚vı ]‰ µo[„Z ]ı˚ı µ „’}µ „˚
2 
t
 
restau rat ion d el'imaged esau vegard e
3 
t
 
restau rat ion d esd on n ée scor resp on d ant au  
D elta 
ent rela créat ion d e 
l'imagesou rceet lad ated elarestau rat ion
58
59


# Page 31

13/09/2024
30
60
Sauv egarde , Restaurat io n, Dispo nibilit é
Mis een placed'un pla n des a uvegarde
Sauvegarde/ Rest a ura tion
Démo
TP3
Mod ule 0 4  

Sauvegar derdes m achines vir tuelles avecVeeam
Sauvegarde,Restaur ation, 
Disponibilité
60
61


# Page 32

13/09/2024
31

Veeam
Back u p
&
Repl icat io n
est
un
log i ci el
de
sau veg arde
de s
do n n é e s
et
de
repr i se

po u r
les
m a ch ine s
vir tu el le s
VMw are
vSphere
et
Microsof t

.

Pri se
en
cha rge
du
pro to cole
VS S
po u r
la
s au vegard e
de
ba s es
de
d o n n é es
Micro sof t

De
n o mbreu ses
fon ctio n n alités
de 
sau vegarde
so n t pr ises
en  
cha rge
Présenta tion :Solution Veeam
Veeam
 
Backup
 
&
 
Replication


S
R
V

NAS
62
63


# Page 33

13/09/2024
32


S
R
V

NAS

SIT
EA
SIT
E 
B
interc onnexion

Ra patr ier
les
sau vegardes
de
 
du
site
B
ver s
le
site
A
par

du  
lien
WA N.
Veeam 
Backup
 
&
 
Replication
 
da ns
 
un
 
cadr e
 
m ulti
-
site


S
R
V

NAS

SIT
EA
SIT
E 
B
interc onnexion

M i s e
 
en
 
p l a c e  
ˆ [µ v
 
N A S
 
su p p lém entaire
 
s u r
 
le
 
site
 
et
 
u t ilisat ion
 
du
 
S e r ve u r  
Vee am
 
du
 
site
 
A
Veeam 
Backup
 
&
 
Replication
 
da ns
 
un
 
cadr e
 
m ulti
-
site
S
R
V

NAS
-
2
64
65


# Page 34

13/09/2024
33


S
R
V

NAS

SIT
EA
SIT
E 
B
interc onnexion

On
 
p ou rrait
 
p otent ielle ment
 
ajo u ter
 
un
 
s e r ve u r
 
Vee am
 
su r
 
le
 
d e u x i è m e
 
site, 
ent raîn ant
 
p a r
 
la
 
m ê m e
 
occasion  
un
 
su rcoû t
 
d e  
licen ces
Veeam 
Backup
 
&
 
Replication
 
da ns
 
un
 
cadr e
 
m ulti
-
site
S
R
V

NAS
-
2



S
R
V

NA S

SIT
EA
SIT
E 
B
interc onnexion

On
 
p ou rrait
 
p otent ielle ment
 
ajo u ter
 
un
 
s e r ve u r
 
Vee am
 
su r
 
le
 
d e u x i è m e
 
site, 
ent raîn ant
 
p a r
 
la
 
m ê m e
 
occasion  
un
 
su rcoû t
 
d e  
licen ces
Veeam 
Backup
 
&
 
Replication
 
da ns
 
un
 
cadr e
 
m ulti
-
site
S
R
V

NAS
-
2

ADMIN
VE
E
AM
Bac
k
up  
Proxy
66
67


# Page 35

13/09/2024
34

Avan t
to u te
cho se,
il
faud ra
définir
les
différen ts
su pp o r ts
de
sto ckag e
dan s
la 
par tie
Backu p
Repo sito ries
et les
assign er.

Disqu es
locau x

Par tag es
NFS

Par tag es
CI FS
/
SMB

Disques
dur s


Il
est 
p o ssible
de
:

Sau vegarde

des
VM

E xclu re 
cer tain sdisqu es

Ch o isir 
le
mo de
de
Backu p
o
I n cremen tal
o
Rever se
I n cremen tal
BackupVeeam
Mise en place des J obs
68
69


# Page 36

13/09/2024
35
Mise en place des J obs

La
 
con figu ra ti o n
 
d e s
 
aler tes
 
m a i l
 
p e r m e t
 

 
d e s
 
ra pp o r ts
 
p o u r
 
les 
Backu ps
 
et 
Réplicatio n s (mo du le 08).
71
Sauv egarde , Restaurat io n, Dispo nibilit é
Sauvegarde/ rest a ura tio na vecVeea m
Démo
TP4
70
71


# Page 37

13/09/2024
36
Module 0 5  

Les stockages 
-
 
Méthodes de réduction des 
données
Sauvegarde,Restaur ation, 
Disponibilité
73
Sauv egarde , Restaurat io n, Dispo nibilit é

Infra s tr ucturedes a uvegarde

Suppo r ts des a uvegarde

Co mp ress ion/ déduplica tio n
St o ckage 
-
 
Méthodesde r éduct ion des do nn ées
72
73


# Page 38

13/09/2024
37
74
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Infr ast r uctur ede sauvegardes 
Po u r mettreen place u n e
sau vegarde, un einfrastru ctu re log icielle 
et matérielle est n écessaire.
Lapar tie m at érielle

Les su pp o r tsdesau vegarde

Les lecteu r s et la ro bo tiqu ede sau vegarde 
Lapar tie logicielle

Le log iciel de sau vegarde

Le log iciel cha rgé delan cer les sau vegardes, app elé 
o rdo n n an ceu r.
75
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Infr ast r uct ur ede sauvegar des 
Les suppor tsdesauvegar de
I l y aplu sieu r s critères àpren dreen compte po u r ch o isir le o u les 
su pp o r tsdesau vegarde
les
mieu x adap tés au périmètre dela 
sau vegardedo n n ées :

La capacité de sto ckag e

La fiabilité du sup po r t

Le tempsd'accès en lectu re / écritu re

La con so mmation électriqu e

La sécur ité
74
75


# Page 39

13/09/2024
38
76
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Infr ast r uct ur ede sau vegar des
SO LUT I O N DAS 
Les so lu tio n s d esto ckag e d etype DA S (Direct 
Atta ched
 
Sto ra g e) co n sisten t àco n n ecter d irectemen t u n p érip h ériq u e 
au ser veu r o u  àla stat io n  d etr avail. 
I l s'ag it p rin cipalemen t d 'u n lecteu r d e ban d esmag n étiqu es 
mais d 'au tresso lu tio n s p eu ven t êtreen visag ées co mme le 
su p p o r t o p tiqu eo u les d isq u es d u r sextern es. 
77
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Inf r astr u ct u r ede sau vegar des 
Le m a tér iel exista nt 
La 
bandem ag nétique 
-
su pp o r t utilisé depu is 195 0 po u r le sto ckag e 

-
deux types de ban des: h élicoïdale et linéaire
Ava nta ge s
-
capacité desto ckag e impo r tan te
-
au to matisatio n  avec les ro bo tsde sau vegardequ i 
accepten t plu sieu r s ban desmagn étiqu es do n t le 
cha rgemen t est au to matisé. 
76
77


# Page 40

13/09/2024
39
78
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Infr ast r uct ur ede sauvegar des 
Suppor t
Atouts
Lim ites
CD / DV D

Peu enco mbr ant

Peu co uteux

Durée de vie faible

Capacité de sto ckage faible
B LU
-
R AY

Durée de vie faible
Disque dur  HDD

Simplicité d'utilisatio n

Peu co uteux

Sensibilité aux cho cs
Disque dur  SSD

Simplicité d'utilisatio n

Prix en baisse

Resistance au cho c

 
Clé USB

Résistance au cho c

Co ût faible

Capacité de sto ckage limité
Car te mémo ire

Résistance aux cho cs

Capacité de sto ckage faible
79
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Suppor t
Atouts
Lim ites
B andes 
magnétiques

Durée de vie élevé

Large gamme de cho ix

R isque d'erreur de manipulatio n
Techno lo gie R DX

Simplicité d'utilisatio n

R isque d'erreur de
manipulatio n

F ragilité
NA S



Redo ndance via le R A ID

Enco mbrement du réseau
SA N

Sécurisation des do nnées

Simplicité d'administration

Pro blèmes d'intero pérabilité


Clo ud

F ichier s accessibles à to ut 
mo ment

Données pro tégées

Per fo rmance dépendant de la 
co nnexion utilisée

Per te de co ntrô le sur les 
do nnées

V itesse de transfer t réduite
78
79


# Page 41

13/09/2024
40
80
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Infr ast r uct ur ede sauvegar des 
Sauvegar desur bandem ag nétique
D D S 
-
 
DAT
 
: DDS (Digital Data Sto ra ge) est le n o mofficiel dela 
DAT (Digital A u dio Tap e)
D LT  

 
SDLT
 
:
Digital Lin ear  Tap e
(DLT, an cien n emen t n o mmée 
CompacTape
)
LTO 
:
Lin ear
 
Tap e
-
Open
(ou
LTO
) est un e
techn iqu e
de sto ckag e 
su r
ban demagn étiqu e
au
for mato u ver t.
81
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Infr ast r uct ur ede sauvegar des 
Sauvegar desur bandem ag nétique
 
 

 
Go

Go


Go

Go
 

Go

Go
 

Go

Go
DLT
-


Go

Go
 

Go

Go
 

Go

Go
SDLT 3 / DLT
-


Go
1600
Go
 
 
 
1 9 2 To
 
 
 
 
 
 
 
 
 
 
 
 
 
 
6  To
 
 
 
 
 
 
 
80
81


# Page 42

13/09/2024
41
82
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
S AN
N AS
Significatio n
Sto ra ge Area  N etwo rk
N etwo rk 
Atta che d
 
Sto ra ge
Pro to co les
SCSI, F ibre Channel o u SATA .
Ser veur de fichier s, NFS o u CIFS.
Par tage de 
 
Le par tage de fichier repo se sur le 

Permet un par tage plus impo r tant 

(Unix et NT).
Identificatio n 
des do nnées
Identifie les do nnées par b lo c de 
disque.
A dresses les do nnées par le no m 

Eligibilité au 
dispo sitif
Périphériques de classe ser veur s do tés 
du canal 
F ibre Channel SCSI
.
Périphérique co nnecté au réseau 
lo cal, do té des pro to co les NFS, 
CIFS/SM B , HT TP o u HT TPS
Co ût et 
co mplexité
Cher et plus co mplexe.
Rentable et mo ins co mpliqué.
Infr ast r uct ur ede sauvegar des 
Sauvegar desur NAS / SAN
83
Sauv egarde , Restaurat io n, Dispo nibilit é
Pl a n de s a uvega rde
Réalisat ion  des sauvegar des
Sauvegar deLocale
Directemen t réalisée su r le site d'explo itatio n , su r un su pp o r t lo cal, les 
do n n éesn e so r ten t pasdu réseau  intern ede l'en trepr ise.

Ser veur de sto ckage dispo nible sur le réseau

Disque dur

B ande magnétique (externalisation du suppo r t physique)
Sauvegar dedistante ou externalisée
Réalisée en deho r sdu site d'explo itatio n , ver s u n site distan t ou  su r 
I n tern et via u n econ n exio n sécur isée, les do n n éesso r ten t du réseau  
intern e del'en trepr ise.
82
83


# Page 43

13/09/2024
42
84
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Réduct ion  du vo lume dedo nn ées
Lacom pression
Permet derédu irele vo lume dedo n n ées.
Les algo rith mes decompression  so n t ch o isis selon  3 critères
:

Le tau x decompression  : rap po r t de la taille du fichier compressé su r 
 

La qu alité decompression  : san so u  avec per te (le % de per teest 
n écessaire)

Les vitesses decompression  et décompression
85
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Réduct ion  du vo lume dedo nn ées
Ladéduplication
Réalise u n référen cemen t des élémen ts iden tiqu es au sein des do n n ées 
sau vegardées afin  d'éviter les do u blo n s:

Ch aqu efichier est déco u péen  tro n çon s

Ch aqu etro n çon àu n  iden tifian t u n iqu e

Ch aqu eiden tifian t est sto cké dan su n  ind ex

Si u n tro n çon existe dan s l'in dex il n'est passau vegardé mais remplacé 
par
un po inteur  ver sl'ident ifiant correspo ndan t
84
85


# Page 44

13/09/2024
43
86
Sauv egarde , Restaurat io n, Dispo nibilit é
Sto ckage 
-
 
réducti o n de do nnées
Dédup lication
Avantage :

Rédu ctio n de l'espace de 
sto ckag e (en mo yen n edivisé par  
20 o u 30)

Co n so mmation de la ban de 
passan te
I nconvénients:

Co n so mmation de CPU

Hash Tab le =SPOF

Regrou pement des don nées= 
plu s derisqu e de per te

Peu t en tr ain er un e per tedu  
for matde do n n ées
Mod ule 0 6  

La sauvegar dede ser veur sLinux
Sauvegarde,Restaur ation, 
Disponibilité
86
87


# Page 45

13/09/2024
44
88
Sauv egarde , Restaurat io n, Dispo nibilit é

«

!»

Vra imen t ?

Stable ne signifie pas infaillible.

 





Et 
que dire du piratage ?
S a uvega rder des  s er veurs  Li nux
Sauv egarde , Restaurat io n, Dispo nibilit é
Sauvegarder un e VM 
ser veur Linu xavec Veeam.
88
89


# Page 46

13/09/2024
45
90
Sauv egarde , Restaurat io n, Dispo nibilit é



-
V il est to u t à 
fait simple dela sau vegarderavec Veeam.
S a uvega rder des  s er veurs  Li nux
91
Sauv egarde , Restaurat io n, Dispo nibilit é

 

Celu i
-
ci offre des o pt ion savan cées derécup éra tio n s n o tammen t

https://
helpcenter.ve ea m. co m
/do c s/
ag entfo r li nux
/
us ergu ide
/
o ver v i ew.h tm l
S a uvega rder des  s er veurs  Li nux
90
91


# Page 47

13/09/2024
46
92
Sauv egarde , Restaurat io n, Dispo nibilit é


S a uvega rder des  s er veurs  Li nux
Sauvegarde,  R estauration, D isponibilité
Sauv egarder les donn ées 

Rsync
92
93


# Page 48

13/09/2024
47
94
Sauv egarde , Restaurat io n, Dispo nibilit é

 
gérer les sau vegardes / restau ra tio n sde do n n éesso u sLin u x est 
r syn c
 
, po u r 
rem o te
 
synch ro nisatio n

Cette comman deva permettre«
basiqu emen t
» d e syn ch ro n iser le 
contenu de deux fichier s ou dossier s. 

On  va do n c«
syn chro n iser
» la co p ie d etr avail avec u n d o ssier o u  
 
 
 
NB :
 

 
S a uvega rder des  s er veurs  Li nux
95
Sauv egarde , Restaurat io n, Dispo nibilit é


Test de con n exio n avec 
cifs
S a uvega rder des  s er veurs  Li nux
user@linux
~ $ mount 

t 
cifs
-
o username=
user 
//
srvfic
/share /mount/point 
Password for user@//
srvfic
/share:********
user@linux
~ $ touch /mount/point/
fictest
user@linux
~ $ ls 

l /mount/point/
fictest
-
rwxr
-
xr
-
x 1 user user 0 2 mars 11:15 
fictest
94
95


# Page 49

13/09/2024
48
96
Sauv egarde , Restaurat io n, Dispo nibilit é
Opt ion n el : Mo n tag eperman en t ou prêt à emplo i

Créer un fichier con ten an t les 
credent ials
 
 
par tag e
S a uvega rder des  s er veurs  Li nux
root@linux
~ # vim ~/.creds
username=
user
password=
monmotdepasse
root@linux
~ # 
chmod
go
-
rwx
~/.creds
97
Sauv egarde , Restaurat io n, Dispo nibilit é

Synchron iser ses don néesavec 
r sync
 
avec compression

 
S a uvega rder des  s er veurs  Li nux
user@linux
~ $ 
rsync
-
avz
/source/
cible
96
97


# Page 50

13/09/2024
49
98
Sauv egarde , Restaurat io n, Dispo nibilit é

 
r syn c

Sauv egarder le co ntenu de mo n ho me ver s un po int de mo ntage



Restaurer un do ssier
S a uvega rder des  s er veurs  Li nux
rsync
-
av 
$HOME /
mnt
/save/$USER
rsync
-
av 
/
srv
/data user@10.6.6.6:/data/saves 
rsync
-
av 
user@10.6.6.6:/data/saves/doss/ /
srv
/data/doss/ 
99
TP
Sauv egarde , Restaurat io n, Dispo nibilit é
Sauvegarderun ser veurLinux 
a vecRSYN C
5
98
99


# Page 51

13/09/2024
50
Module 0 7  

La r edondancede données 
-
 
RAID
Sauvegarde,Restaur ation, 
Disponibilité
102
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
L a r edo n dan ce dedo n n ées
Co n siste à d u p liq u er d esco mp o san ts o u d es d o n n éesessen tielles d 'u n  
système, avec p o u r o b jectif d 'amélio rer sa fiab ilité.
Fonctionnem ent :

Peu t êtredéfinie via u n econ figu ra tio n  matérielle o u log icielle

L'o bjectif est de po u vo ir recon str u ireles do n n éesen  cas dedéfaillan ce du  
système
100
102


# Page 52

13/09/2024
51
103
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées

D isques dur s
: techn o log ie
Ra id, o n répar titles do n n éessu r u n en semble de 
 
des disqu es.

Ser veur s
 
: réplicatio n  en  tempsréel des do n n ées
en tredeux ser veu r s o u  
c lus tering
 


Multisite
 
:
effectu er la redo n dan cesu r plu sieu r s
sites
po u r palier
u n inciden t 
majeu r

104
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
RAI D  :
Redundant
Array
of I ndependent
Di sks
Techn iqu e de par tition des do n n éessu r plusieu r s disqu es du r spo u r au gmen ter

la to léra n ce au x pan n es

la sécur ité

la répar tition et la coh éren cede ces do n n ées
Le système RA I Dpeu t êtrelog iciel o u matériel
103
104


# Page 53

13/09/2024
52
105
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
RAI D  :
Lo giciel
Le con trô ledu RA I Dest assu réà 100 % par u n ecou che log icielle du système 
d'explo itatio n .
Avantages

Techn iqu e la mo ins o n éreu se

Sou plesse d'ad min istr atio n

Co mpatibilité en treto u tesles machin es équ ipées du même con trô leu r RA I D(OS)
106
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
Le RAI D  0 est aussi appelé
St ri pingo uEnt rel acement .

Co n stitu éd'u n min imu m de 2 disqu es du r s.

Co n siste à diviser les do n n éesen blo cs et à répar tirces 
 
gr ap pe.


RA I D0 defou rn ir debo n n esper for man ces en Lectu re/ 

disqu es du r s.
105
106


# Page 54

13/09/2024
53
107
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
Le RAI D  1 est aussi appelé
Mirro ri ng.

I l se con stitu esu r 2 disqu es du r set co n siste à 
répliqu er les do n n éespo u r les écrire su r les deux  
disqu es du r s.

Cette o pératio n de réplicatio n  a po u r co n séqu en ce 
de rendremodéréesles per for mancesde Lecture/ 
É critu re.

 
disqu e du r.
108
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
RAI D  5

Le RA I D
 
5 se con stitu e su r un min imu m 
de 3 disqu es du r s.

U tilisatio n  simu ltan ée des disqu es du r s 
qu i compo sen t la gr ap peren dan t les 
per for man ces bo n n esen Lectu reet 
mo déréesen  É critu re.

De plu s, u n erépar tition dela par itéen  
cascade permetau RAI D5 un etoléran ce 

107
108


# Page 55

13/09/2024
54
109
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
RAI D  6

Le RA I D6 se con stitu e d'u n min imu m de4 disqu es du r s.

U tilisatio n  simu ltan ée des disqu es du r scomme po u r le RA I D5.

Dou ble répar tition dela paritéen cascade, augmentela
toléran ce depann eà 2 
disqu es du r s.
110
Sauv egarde , Restaurat io n, Dispo nibilit é
Pl a n de s a uvega rde
La r edo ndance dedo nn ées
109
110


# Page 56

13/09/2024
55
111
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
RAID  1 0

Le RA I D10 se con stitu e d'u n min imu m de 4 disqu es du r s.

Lier des gr ap pesRA I D1 so u su n e gr ap peRA I D0.

Bo n n eper for man ce en Lectu re/ É critu re

To léra n ce de pan n ede1 disqu e du r par so u s gr ap peRA I D1
112
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
La r edo ndance dedo nn ées
111
112


# Page 57

13/09/2024
56
113
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
RAID
L a r edo n dan ce dedo n n ées
Synth èse s u r l atech n ol ogieRA I D
RAID 0
RAID 1
RAID 5
RAID 6
RAID 10
Nbr minimum 
de
disques
2
2
3
4
4
To léranc e de 
panne
Pas de 
pro tec tio n ( 0)
Panne 1
disque
Panne 1 disque
Panne 2
disques
Panne 1 disque 
par so us grappe 
R AID 1
Perfo rmanc es 
en lec ture
élevées
élevées
élevées
élevées
élevées
Perfo rmanc es 
en éc riture
élevées
mo yenne
faible
faible
élevées
Utilisatio n de la 
capac ité
100%
50%
67%
-
94%
50%  
-
 
88%
50%
114
Sauv egarde , Restaurat io n, Dispo nibilit é
RAID
Démo
TP6
113
114


# Page 58

13/09/2024
57
Module 0 8  

La r edondancede données 
-
 
Clustering
Sauvegarde,Restaur ation, 
Disponibilité
116
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
Cl us teri ng
LeClust ering
Cl u ster d e ser veu rs

Un clu ster d eser veu rs ou grap p ed eser veu rsest u n grou p ed esystème sinfor mat iq u es 
]v ˆ  › ˚v ˆ vı µ vˆµ ı „ › › ˚oŠv ‹µ ˆ}µŠ
n od es
",q u ifon ct ion n ent 
˚v ’˚u}u ’[P]’’]ıˆ [µ v’˚µ’Ç’ı˜u˚› }µP„vı‰ µˆ› › o]ı ]}v˚ı 
d esresso u rcescrit iq u esrestent d isp on ib lesp ou rlesclient s.

Les clu stersd eser veu rsp er mettent au xclient s
ˆ [ ˆ ˚„µ Æ v ‹µ ˆ˚ıˆP „˚„
n on com med esord in ateu rsd ist in ct s,maiscom meu n seu let  u n iq u esystème .
115
116


# Page 59

13/09/2024
58
117
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
Cl us teri ng
LeClust ering
La resso u rceq u or u m

Présented an stou t clu ster

Con ser ve
lesd on n ée sd econfigu rat ion n écessairesàlarécu p érat ion d u clu ster.

jo u rn au xd erécu p érat ion ,contie n n ent d esinfor mat ion sd étaillée ssu rtou tesles 
mo d if icat ion sap p or tée sàla b ased ed on n ée sd eclu ster.
 ˚ıı„˚’’} µ „’ı}lPˆˆ }v v  ˚ˆ}v(]Pµ „ı ]}v˚ıˆ [ııˆ µoµ ’ı˚„˚’ı 
]v ˆ  › ˚v ˆ vıˆv ‹µ ˆ ’X
118
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
Cl us teri ng
LeClust ering
A p p or td es cl u sters
Hau te d i sp on i b i lité(
avai l ab i l i ty
)

D on n ée sd u clu ster garant iesd isp on ib lesà99 ,9% d u temp s.

µ vˆv ‹µ ˆv› ˚µ ı› oµ(}µ „vˆ„ › }vµ Æ„˚‰ µ !ıˆo]˚vıo} „
µ ı „v ‹µ ˆ› „˚v v ˚vı„˚o ]’X
A d ap tab i l i té
(
scal ab i l i ty
)

˚’ı› }’’]ˆ [i} µ ı˚„

µ v› oµ ’]˚µ „v ‹µ ˆ ’U

ˆ„˚’’} µ „› ZÇ’]‰ µ~ˆ]’‰ µ› „}˚’’˚µ „u u} ]„À]À µ Æv ‹µ ˆ ’
117
118


# Page 60

13/09/2024
59
119
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
Cl us teri ng
LeClust ering
A rch i tect u red escl u sters

Le clu ster in gcon sisteà assemb ler d esser veu rs en grap p eq u iu t ilised esp ér ip h ér iq u es 
com mu n savec u n eévent u elle rép art it ion d elach arged et raiteme nt .

Les resso u rcesd estockaged oivent êt recom mu n eet u n b u s
ent relesd ifférent s 
v ‹µ ˆ ’
est n écessaire
120
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
Cl us teri ng
Typede Clust er
Le cl u ster à b ascu l ement:
Le fai l over
ˆ (ˆ Œµvv ‹µˆ› ˚„u˚ı ’µµ ı}uı ]‰ µˆı}µ ı„˚’’}µ „
À˚„ oŒµ ı „v ‹µ ˆˆ µoµ ’ı˚„
1 
-
 
Le clien t en voie u n e req u ête s u r le s er veur vir tu el g éré par 
 
2 
-
 
 
s er vice 
3 
-
 
 
h ear tbeat
 
»s u r le rés eau privé 
 
 
4 
-
 
 
s er veur vir tu el 1 pou r les  clien ts  extern es  
5 
-
 
La req u ête clien t es t alor s  correctemen t ach eminée et la 
 
S e r ve ur V ir tue l1
QUORUM
Disque 1
Disque 2
1
2


He artbeat
4
5
3
119
120


# Page 61

13/09/2024
60
121
2
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
Cl us teri ng
Typ edeClust er
Le cl u ster à b ascu l ement:
Le 
fai l b ack
  „ı ]}v}v ’]’ıvı „˚u˚ıı „µ vv ‹µ ˆ˚v› „}ˆ µ ı ]}v› „u]vı˚v v }µ
n ivea u
1 
-
 
 
es tremis  en  prod u ction.
2 
-
 

 
3 
-
 
 
 
lui s on t alor s  res tit u é.
4 
-
 

vir tu el  (d on t l'IP n'a pas ch ang é). 
5 
-
 
Les  clien ts  peu vent  con tin u er à f aire leu r req u ête, et le 
f ailback
 
res te inv is ible 
d u  côté clien t, on  peu t n oter par f ois  en  f on ction d es application s  u tilis ées  u n e 
micro
-
cou pu re
 
d e con n exion  au s er veur
S e r ve ur V ir tue l1
QUORUM
Disque 1
Disque 2


He artbeat
1
4
5
3
122
Sauv egarde , Restaurat io n, Dispo nibilit é
La  redonda nce de do nnées  
-
 
Cl us teri ng
Typ edeClust er
Le cl u ster à éq u i l i b raged ech arge:
Le "
l oad
 
b al an ci n g"
En semb led etech n iq u esp er mettant d erép art iru n ech arged et ravail
t rop  
imp or tante
ent red ifférent sser veu rsd u clu ster p ou rréd u irel'in d isp on ib ilitép otent ielle  
du
ser vice.
121
122


# Page 62

13/09/2024
61
Sauvegarde,  R estauration, D isponibilité

cluster avec HAproxy
124
Sauv egarde , Restaurat io n, Dispo nibilit é



des rever seproxyavec équ ilibra ge de cha rgeen h au te 
dispo n ibilité

La ver sion LTS 
202
4
 
est la 
3. 0
 
. Cycle de vie de5 an s. 

Site web : 
h ttp s://h ap roxy.o rg
 

Dépô t : 
h ttp s://g ith u b. com/h ap roxy

Do cumenta tio n  : 
h ttp ://d o cs.h ap roxy.o rg/
 

 
h ttp s://www.h ap roxy.co m/fr/b log /th e
-
fou r
-
essen tial
-
sectio n s
-
of
-
an
-
h ap roxy
-
con figu ra tio n /
 
123
124


# Page 63

13/09/2024
62
125
Sauv egarde , Restaurat io n, Dispo nibilit é


U n ser veu r HA Proxyjou e les rô les su ivan ts :

Rever se Proxy: capter les requ êtesweb des clien ts

Load
 
 
 
126
Sauv egarde , Restaurat io n, Dispo nibilit é


I nstallation  de HAp roxy

HA proxy est dispo nible dans les dépô ts standards des distributio ns Linux

O rac leLinux 8

D ebian 11
125
126


# Page 64

13/09/2024
63
127
Sauv egarde , Restaurat io n, Dispo nibilit é





Les CNA ME po u r les sites web po intero n t ver s ce 
h ap roxy
128
Sauv egarde , Restaurat io n, Dispo nibilit é

Dans le fichier /
etc
/
hap roxy
/
h aproxy.cfg
,configurer :

fro nt
-
end
  
avec réseau x en écou te et définitio n  du /des backen d

bac k
-
end
 



au tres, san s n o tio n de backu p
frontend frontend
-
web
default_backend
backend
-
web
bind *:80
#
Ecoute
sur 
toutes
les 
adresses
backend backend
-
web
server web1
10.100.1.1:80 check
server web2 10.100.1.2:80 check
server web3 10.100.1.3:80 check
127
128


# Page 65

13/09/2024
64
129
Sauv egarde , Restaurat io n, Dispo nibilit é

Dan s le fichier /
etc
/
h ap roxy
/
h ap roxy.cfg
,con figu rer :

fro nt
-
end
  
avec réseau x en écou te et définitio n  du /des backen d

bac k
-
end
 


 
 
frontend frontend
-
web
default_backend
backend
-
web
bind *:80
#
Ecoute
sur 
toutes
les 
adresses
backend backend
-
web
server web1
10.100.1.1:80 check
server web2 10.100.1.2:80 check
server web3 10.100.1.3:80 check backup
130
Sauv egarde , Restaurat io n, Dispo nibilit é


Tester le fichier

-
c 
check

-
f
 
 
file 

A ctiver le ser vice au démar ra ge 
du ser veu r

Vérifier le fon ctio n n emen t du ser vice
# 
haproxy

c 

f /
etc
/
haproxy
/
haproxy.cfg
# 
systemctl
enable haproxy
# 
systemctl
status 
haproxy
-
l 
--
no
-
pager
# curl http://
www.monentreprise.tld
129
130


# Page 66

13/09/2024
65
131
Sauv egarde , Restaurat io n, Dispo nibilit é
H a proxy
 
da ns  une a rchi tec ture a ppl i ca ti ve

E n en trepr isela plu par tdes ap plicatio n s web ut ilisen t u n ebase de 
do n n ées. 

Dan s le cadre dece cou r s, les diver s ser veu r s web/a pp li 
tr availlero n t to u s avec la même basede do n n ées.
132
TP
Sauv egarde , Restaurat io n, Dispo nibilit é
Equilibr a gede c ha rges ur 
deuxs er veur s web
7
131
132


# Page 67

13/09/2024
66
Module 0 9  

 
La r éplication deVM
Sauvegarde,Restaur ation, 
Disponibilité
134
Répl i ca ti o n de VM
S auvegarde, Rest auration, Disponibilité

La
 
rép licat ion
 
est
 
une
 
solu t ion
 
de
 
récu p érat ion
 
ˆ [µ „P˚v ˚
 
en
 
cas
 
de
 
d éfaillan ce 
matér ielle
 
ou
 
de
 
crash
 
système .

Elle
 
p e r m et
 
une
 
remise
 
en
 
état
 
rap id e
 
du
 
s e r v i c e
 
en
 
d éma rrant
 
le
 
rép lica
 
de
 
la 
m a c h i n e
 
imp actée .

L e s
 
rép licas
 
d evront
 
ob ligatoirement
 
êt re
 
stockés
 
sur
 
un
 
d atastore
 
ESXi
 
o u  
Ç›˚„>
 
mo nté.

La
 
taille
 
du
 
rép lica
 
est
 
id ent iq u e
 
à
 
celle
 
de
 
la 
V M .
Réplication de V M
133
134


# Page 68

13/09/2024
67
135
Répl i ca ti o n de VM
S auvegarde, Rest auration, Disponibilité

 ]v   ˚ ’ ’  ] „˚ i } µ ı˚o [ ZÇ › ˚ „ À ] ’˚ µ „ ]  o ˚˚ ˚  u
Réplication de V M
136
Répl i ca ti o n de VM
S auvegarde, Rest auration, Disponibilité

C ré e r u n j o b d e ré p l i cat io n  

S é l e c t i on n e rl a  V M s o u rc e

[˚ u › o  ˚ u˚ vı ]  o ˚

P ré c i s e rl e s o p t i on s d u j o b &  l a  
ré c u r re n c e
Réplication de V M
135
136


# Page 69

13/09/2024
68
137
Répl i ca ti o n de VM
S auvegarde, Rest auration, Disponibilité
Un
 
rép lica
 
ne
 
do it
 
pas
 
être
 
démar ré
 
man u ellemen t
 
mais
 
u n iqu emen t
 
via
 
la 
con so le 
Veeam
 
Backu p
 
&
 

Replic a
 
To o ls
.


Cette fon ctio n n alité
 
est 
un 
é l é m e n t  
clé dan s les 
calculs 
de
 
RTO.

U n e  
fois 
la 
V M  
e n d o m m a gé e  
remise
 
en
 
état , 
on
 
peu t
« 
merger 
» 
les 
2 
V M  
po u r 
éviter 
la 
per te
 
de
 
do n n ées.
138
TP
Sauv egarde , Restaurat io n, Dispo nibilit é
Mis een placede la réplica tio n 
deVMa vecVeea m
8
137
138


