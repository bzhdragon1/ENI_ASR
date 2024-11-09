# Page 1

Adminis tra teur
-
triceSystèmes et Rés eaux
 
 
Pa g e 
1
 
s ur 
4
 
© ENI  

 
T ous  d roi t s  ré s e rvés
 
 
Création de l'infrastr ucture
 
TPdu 
M
o dul e 
0
1
 

 
Concept,Enjeux,définition
 
 
 
suivi le
 
module 
1
.
 
V Mwar e Works tationdoit êtr e installé s ur votre mac hine des alle.
×
 
 
V ous deve z avoir accès au 
par tage dis trib.
×
 
 
D u r ée estim ée
 
2
 
à  3 
heure
s
 
Én oncé
 
En  vou s b asan t su r les in for mat ion sf ou rn ies ci
-
d essou s, vo u
s cré er ez  
o[˚v À]„} v v˚u˚ vıˆ 
maq u et t age 
en u t ilisan t
 
les 
mach ines virtu elle s
 
d isp on ib le
s
 
sur Dist rib  
 
Cet t e arch itect ure  simu le un  
en vironn emen t mixt e
 
: 
 

 
d an s Wor kst at ion  les mach in es «
 
p h ysiqu es
 
»
 
: 
Pfsen se
 
+
 
N AS
 
+
 
ESXi
 
+
 
Se rveu rd eb acku p
 
 

 
µ ’˚]v ˆµˆ o[ o˚’
ser veu rs
 
virt uels
 
SRV
-
AD 1 et SRV
-
FIC1
.
 
 
Im port desmachines  
virtuelles
 
Sc héma d e 
 
 
 
 
L a valeur  
X
 
du
 

VM net12 
c or r es pond au der nier 

 
 
 
E
xemple
 
: 
IP hôte
 
=
 
10.44. 101.
20
 

 
x=20
 

 
IPESXi
 
 
= 
172. 16. 20. 245
 


# Page 2

Adminis tra teur
-
triceSystèmes et Rés eaux
 
 
Pa g e 
2
 
s ur 
4
 
© ENI  

 
T ous  d roi t s  ré s e rvés
 
 
I nst aller les  m ac hines 
"
phys iques
"
 
d ans Workstatio n
 

 
Récu p ér
er
 
lesf ich ier s OVA d ispon ib les 
d an s R:
\
Bun d les
\
ASR20 21
\
M11
-
Sauvegar d e
-
Resta u rat ion
-
D isp on ib ilité_ OVA.
 

 
Cré e
r
 
un e arb orescen ced e stockage d e mach in evirt u elle 
d an s le dossie r
 
D:
\
VM s
 
d e vot re 
mach in e d e salle. Ch aq ue mach in e virt u elle serast ockée  d an su n d ossie rd éd ié.
 
 

 
Imp or te
r
 
dan s Wor kst at ion  
les mach in es virt u elles 
 

 
srv
-
b
acku p
.ova
 

 
t ru en as.ova
 

 
r
ou teu r
.ova
 

 
In st alle r un
e mach in e clien t e
 

 
Récu p ér er su r D istrib u ne mach in e Win d ow s 10pré in st allée
 
: 
 
 
R:
\
image s
-
virt u elles
\
vmw are
\
Win dow s
\
clien t
\
Win d ow s10
\
W10
-
*
-
Base.7z  et  la 
cop ier d an s D :
\
V M s
 

 
OU
 
u n e machin e Deb ian 10  pré in st allé e
 
R:
\
images
-
virt u elles
\
vmw are
\
Lin u x
\
D eb ian 11
-
cinn amon .7z
 
et  la cop ier d an sD :
\
V M s
 

 
Ext rair e le con t en u d e cet t e arch ive, ou vrir laV Md an s Wor kst at ion ,af fecter  la 
cart e ré sea u au V Mn et12 et don ner u n e @IPv4 lib re d an s lep lan 192.1 68 .20 .0/ 24 . 
 

 
 

 
A tt en ti on
 
les machin es SRV
-
AD 1 et SRV
-
FIC1 ser on t  à 
in st alle r
 
ˆ v o[ ı › ˚
su ivan te 
p as d irect ement  d an s Workst at ion
. 
 
 
No m
 
T yp e syst èmes
 
Domai n e
 
A
d r esse I P
 
Login
 
Mot  d e 
p asse
 
Srv
-
b acku p
 
Win d ow s Se rveu r 
2019
 
en i l ab .l cl
 
1
92 .16 8.
10 .2
 
A d mi ni st r ateur
 
Pa$$ w 0rd
 
Nas
 
Fre eb sd 
-
 
T
rue
N AS
 
en i l ab .l cl
 
19 2.16 8.30 .1
 
Roo t
 
Pa$$ w 0rd
 
Rou teu r
 
Fre eb sd 
-
 
P
f sen se
 
en i l ab .l cl
 
19 2.16 8.10 .25 4
 
19 2.16 8.20 .25 4
 
19 2.16 8.
30 .25 4
 
dh cp sall e
 
ad mi n
 
Pa$$ w 0rd
 
S rv
-
ad1
 
Window s Serv eur 
2019
 
eni l ab. l cl
 
1
7
2.16 .
x
.25 0
 
A dmin i strateu r
 
Pa$$ w 0rd
 
S rv
-
fi c1
 
Window s 
Serv eur 
2019
 
eni l ab. l cl
 
17 2.16 . x
.
1
 
A dmin i strateu r
 
Pa$$ w 0rd
 
ESXi
 
V M Ware ESX i7
 
*
 
1
7
2.16 .
x
.24 5
 
Roo t
 
Pa$$ w 0rd
 
Ta blea u 
réca pitula tifd es  machines ,  s ys
tèmes  et co mptes
 
 
Rap p el
 
: 
La valeu r
 
X
 
ˆ µı „}]’]˜ }ı o[ˆ „˚ ’’ µı ’µ o˚ v ˚ı í }„ „˚ ’› µ ˆ˚„ v ]˚„ 
}ı ˚ o[ˆ „ ˆ ˚ À}ı „˚ uZ ]v Z•ı ˚X
 
Exemp le
 
: IP h ôt e
 
=
 
10.44.1 01 .
20
 

 
x=20 

 
IP ESXi
 
= 
172 .16 .20 .245
 
 
NB
 
:
 
l
a V M srv
-
Á˚ X}À v[˚’ı› 
imp ort er p ou rle 
mo men t .
 
 
 
 
 


# Page 3

Adminis tra teur
-
triceSystèmes et Rés eaux
 
 
Pa g e 
3
 
s ur 
4
 
© ENI  

 
T ous  d roi t s  ré s e rvés
 
 

 
puis
 
les VM SR V
-
AD1 e t SR V
-
F I C1
 
 
Se reporter à l a 
 
 
: 
ASR 2021_M 11_Proc ed ure_inst all_E SX i
 
 
Co nfiguratio n rés eau d es machinesv irtuelles
 
 
 

 
Les cart esré seau VM w are sont t oute s con f igu ré es en V
M
n et .
 

 
ESX i
 
 
== > VM n et 12
 

 
Srv
-
ad 1 
 
==> 
VM net ESXi
 

 
Srv
-
Backu p  
 
== > VM n et 11
 

 
Srv
-
f ic1
 
==> 
VM net ESXi
 

 
Tr u en as
 
== > VM n et 13
 

 
Rou t eu r Pf sen se :
 

 
N etwo rk Ad apt er  
 
== > Brid ged
 

 
N etwo rk Ad apt er 2 
 
== > VM n et 11
 

 
 }ˆ ]( ]˚„ o[ˆ „ˆ „ı W ììWìWîõWñW í Wñ 
 

 
N etwo rk Ad apt er 3
 
== > V Mn et 1 2
 

 
 }ˆ ]( ]˚„ o[ˆ „ˆ „ı W ììWìWîõW Wò õ
 

 
N etwo rk Ad apt er 4
 
== > VM n et 13
 

 
 }ˆ ]( ]˚„ o[ˆ „ˆ „ı W ììWìWîõWñW í Wó ï
 
 
Vérific atio n après impo rt
 
: 
 
 i˚ ı ]( ˚’ıˆ }v ı „•o˚ ‰ µv }ı „ ]v ( „’ı „µ ıµ „ ˚’ı }› „ı ]}vv˚ oo˚ ( ]v ˚„ı ]v 
con f igu rat ion s.
 
 

 
Po u r les mach in es «
 
Wind ow s 20 19 
S
erver
 
»
 
au beso in :
 
o
 
Apr ès
 
impo r t
a
tio n
, 
si 
le"
gu es to peratin gs ys tem
" bascu le sur "
o th er
"  et la 
versio n sur  
"
other
"
 
;r
epo sitionn er  le"
gues to peratings ys tem
" sur "
M ic ros o ft Win dows
" et la 
version sur  "
W in do ws s erve r201 6 o u 2 019
".
 
 

 
 
 
 
Allu mer t ou tes lesV M de n ot re inf rast ru ct ure  
 

 
Ou vrir un e session  su rt ou t es vos VM
 
:
 
o
 
Ad min ist rateu r /  
Pa$$w0r d
 
 
 
 


# Page 4

Adminis tra teur
-
triceSystèmes et Rés eaux
 
 
Pa g e 
4
 
s ur 
4
 
© ENI  

 
T ous  d roi t s  ré s e rvés
 
 

 
Dep u i s sr v
-
b ackup   
 
o
 
Ef f ect u er lep in g su ivan t
 
:
 

 
srv
-
ad 1/  srv
-
f ic1/ t ruenas
 
 

 
Pr ép ar ati on d u NA S
 
o
 
Ou vrir 
votre n avigat eu r
,vérif ier q ue le p ort ail w eb  du  serveu rN ASest 
op ér at ionne l
 
:
 

 
r
oo t /  
Pa$$w 0r d
 

 
«
 
Con sole
 
», 
exécu ter  «
 
w b inf o 
-
t
 
› }µ „ À „](]˚„‰ µ ˚ o[]vı  P„ı ˚’ı}l
.
 

 
  v [˚’ı› o˚ ’
 
o
 
Aller  su r le menu «
 
’˚„À] ˆ [v vµ ]„˚
 
» /  «
 
Act ived irect or y
 
»
 
o
 
Op t ion
s
 
Avan cé
es
,
 
f aire  
enregist rer
 
p ou r voirap parait re leb outon  
^
Quit t er le domaine
_
 
(admin ist rat eur / Pa$$ w0r d)
 
o
 
A
c
t u alis
er
 
lap ageet ré int égre r leN as au  dom aine
 
o
 
}Z ˚„ ı ]À˚ ~„˚‰ µ ]˚„ı u}ıˆ›}µ› „]v ]› 
  ˚„
 
o
 
«
 
En re gist re r
 
» p ou r réint égre r leN AS au D om aine
.
 
 

 
«
 
Con sole
 
», re faire  la comman d «
 
wb inf o
 
-
t
 
}µ À „]( ]˚„ ‰ µ o[]v ı  P„ı ]}v 
AD  est  ok
.
 

 
Aller  su r le menu «
 
service
 
» et  act iver le service «
 
ISCSI
 
»
.
 
 

 
Sur  sr v
-
f i c1
 
o
 
Se  conne ct er su r la VM
 
:
 

 
Ad min ist rateu r
 
/
Pa
$$w 0rd
 

 
Ef f ect u er 
lesp in gs su ivan t s
 
:
 
srv
-
ad 1
, 
srv
-
b acku p
, 
t ruen as
 


