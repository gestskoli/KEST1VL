# Æfingaverkefni í forritun með bash
## 1a.
Skrifaðu forrit sem biður notandann um tvær tölur. Forritið leggur svo tölurnar saman og birtir á skjánum.

Dæmi um notkun:
```bash
Sláðu inn tölu a: 7
Sláðu inn tölu b: 8
a + b = 15
```
## 1b.
Breyttu forritinu hér að ofan þannig að notandinn sé beðinn um hvort hann vilji leggja saman eða draga frá. Gerðu valmynd og notaðu case-esac til að greina hvað notandinn valdi.

Dæmi um notkun:
```bash
Sláðu inn tölu a: 12
Sláðu inn tölu b: 8
Aðgerðir:
1: a + b.
2: a – b.
Veldu aðgerð: 2
a – b = 4
```

## 1c.
Bættu margföldun og deilingu við forritið hér að ofan ásamt valmöguleikanum að hætta. Forritið á að spyrja um reikniaðgerðir til að gera á tölunum þar til notandinn velur að hætta. Ekki þarf að biðja um nýjar tölur.
```bash
Sláðu inn tölu a: 12
Sláðu inn tölu b: 8
Aðgerðir:
1: a + b
2: a – b
3: a * b
4: a / b
5: Hætta
Veldu aðgerð: 2
a – b = 4

Aðgerðir:
1: a + b
2: a – b
3: a * b
4: a / b
5: Hætta
Veldu aðgerð: 5
Takk fyrir!
```

## 2a.
Skrifaðu forrit sem biður notanda um nafn á sveitarfélagi og telur svo hversu margir eru skráðir í því sveitarfélagi samkvæmt fakesnames.csv skránni (notaðu cut, grep og wc í forritinu).

Dæmi um notkun:
```bash
Hvaða sveitarfélag viltu skoða: Akureyri
102
```
## 2b.
Breyttu forritinu hér fyrir ofan þannig að það birti meira lýsandi upplýsingar.

Dæmi um notkun:
```basj
Hvaða sveitarfélag viltu skoða: Akureyri
Í sveitarfélaginu Akureyri eru 102 skráðir.
```

## 2c.	
Breyttu forritunu hér að ofan þannig að nafnið á sveitarfélaginu sé tekið inn um leið og forritð er ræst.

Dæmi um notkun:
```bash
$ ./ibuateljari.sh Akureyri
Í sveitarfélaginu Akureyri eru 102 skráðir.
```

## 3a.
Ungur frændi þinn á Eskifirði er að byrja læra margföldun í skólanum og vantar forrit til að skrifa út margföldunar töfluna. Skifaðu fyrir hann forrit sem tekur inn tölu og skrifar svo út á skjáinn 10 sinnum töfluna fyrir þá tölu.

Dæmi um notkun:
```bash
$ ./margfoldunartafla.sh 7
1 * 7 = 7
2 * 7 = 14
...
9 * 7 = 63
10 * 7 = 70
```

## 3b.
Bættu við virkni forritsins hér að ofan þeim möguleika að ef 0 (núll) er tekið inn þá skrifast öll margöldunar-taflan upp í 10 út.

Dæmi um notkun:
```bash
$ ./margfoldunartafla.sh 0
1       2       3       4       5       6       7       8       9       10 
2       4       6       8       10      12      14      16      18      20 
3       6       9       12      15      18      21      24      27      30 
4       8       12      16      20      24      28      32      36      40 
5       10      15      20      25      30      35      40      45      50 
6       12      18      24      30      36      42      48      54      60 
7       14      21      28      35      42      49      56      63      70 
8       16      24      32      40      48      56      64      72      80 
9       18      27      36      45      54      63      72      81      90 
10      20      30      40      50      60      70      80      90      100
```

## 4a.
Giskaðu á töluna er einn af fyrstu tölvuleikjunum sem var skrifaður. Hann virkar þannig að tölvan hugsar sér tölu á milli 1 og 100 og á leikmaðurinn að reyna að giska á hvaða tölu tölvan hugsaði sér.
Til að láta tölvuna hugsa sér tölu er hægt að nota slembitölu (e. random number). Í bash er til fallið `$RANDOM` (sem nota má eins og breytu) sem skilar tölu á bilinu 0 til 32767 og til að fá tölu frá 1 til 100 má nota `slembitala=$((1 + $RANDOM % 100))` þar sem % er modulus eins og í python. Breytan slembitala inniheldur þá einhverja tölu á bilinu 1 til 100.
Skrifaðu bash útgáfu af Giskaðu á töluna.

Dæmi um notkun (rétt tala 31):
```bash
Ég hugsa mér tölu á milli 1 og 100, reyndu að giska á hver hún er: 50
Ekki rétt, of há tala, reyndu aftur: 25
Ekki rétt, of lág tala, reyndu aftur: 31
Til hamingju þú fannst töluna 31 í 3 tilraunum!	
```

## 4b.
Bættu við forritið hér að ofan að notandi er spurður um nafn og ef þitt nafn er slegið inn virkar forritið þannig að leikurinn vinnst alltaf í fyrstu tilraun.


