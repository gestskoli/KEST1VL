# Æfingaverkefni fyrir kafla 10

Sæktu geymsluna (e. repository) sem þetta skjal er í og settu á linux vélina 
þína. Þú getur sótt geymsluna með því að gefa eftirfarandi skipun í linux 
(vertu í heimasvæðinu þínu): 
```bash
git clone https://github.com/gestskoli/KEST1VL.git
```

Í mörgum spurninganna sem á eftir fylgja er vísað í skjalið `fakenames.csv` en 
þú finnur það í rót geymslunnar. Skjalið inniheldur upplýsingar um 3000 
skáldaða einstaklinga. Skjalið er sett upp eins og tafla og eru dálkarnir 
aðgreindir með tab. Í verkefninu æfir þú notkun á grep, cut, wc, nl o.fl., 
til að finna ýmsar upplýsingar um þessa einstaklinga. Þú getur gefið 
skipunina `head -1 fakenames.csv` til að sjá hvaða upplýngar eru skráðar um 
hvern einstakling.

Svaraðu svo spurningunum í þetta skjal. Þú getur opnað það með forritinu `nano`. 
Hafðu tvo linux glugga opna hjá þér.

1. Notaðu `cut` skipunina til að prenta út öll fornöfn (e. given name) í 
skránni.
   
   Svar: 

2. Notaðu `cut` og `sort` skipanirnar til að fá öll fornöfnin í stafrófsröð, 
passaðu að ekkert nafn birtist oftar en einu sinni. Skrifaðu svo fornöfnin 
svo í skrána `fornofn.txt`.

    Svar: 

5. Hvenær er betra að nota `more` skipun í stað `cat` þegar þú ætlar að skoða 
innhald skráar?

    Svar: 

6. Notaðu `less` skipunina til að finna nafnið "Helgi" í fakenames.csv skránni.

    Svar: 

7. Hver er munurinn á `head` og `tail` skipuninni í linux?

    Svar: 

8. Sýndu fyrstu 3 línurnar í fakenames.csv skránni með `head` skipuninni.

    Svar: 

9.  Sýndu síðustu 4 línurnar í fakenames.csv skránni með `tail` skipuninni.

    Svar: 

10. Notaðu `grep` skipunina til að finna allar línur sem hafa stafina “eim” í 
fakenames.csv.

    Svar: 

11. Notaðu `grep` skipunina til að finna allar línur sem byrja á tölustafnum 4.

    Svar: 

12. Hvað gerir þessi skipun/skipanir: `grep '.y' fakenames.cvs`?

    Svar: 

13. Hvað gerir þessi skipun:  `grep -E 'Jenný|Vaka|Elsa' fakenames.csv`?

    Svar: 

14. Hvað gerir þessi skipun: `egrep 'Unn(a|u)r' hallo.txt`?

    Svar: 

15. Hvað gerir þessi skipun: `head fakenames.csv | grep '[0-9]'`?

    Svar: 

16. Hvað gerir þessi skipun: `grep -E '[0-9]{3}' fakenames.csv`?

    Svar:

17. Ef þú breytir skpuninni hér að ofan í `grep -E '\s[0-9]{3}\s' fakenames.csv` 
hvað breytist þá? Hvað gerir `\s`?

    Svar:

--------------------------------------------------------------------------------

Í liðnunum hér á eftir átt þú að finna upplýsingar um einstaklingana sem eru í 
`fakenames.csv` skránni. Við hvern lið skrifaðu skipunina eða skipanirnar sem
þú notaðir til að leysa liðinn.

18. Búðu þér til nýja skrá (dalkar.txt) sem inniheldur nöfnin á dálkunum og 
svo númer hvað þeir eru:
        1  Number
        2  Gender
        3  GivenName
        ...
        17  Kilograms
        18  Centimeters
        19  Birthday

    Skipun: 

19. Hversu margir einstaklingar búa í póstnúmeri (ZipCode) 601? 
        Svarið ætti að vera 23.

    Skipun: 

20. Hvað heita þeir, sýndu fornafn (GivenName) og eftirnafn (SurName)?
        Boði    Sigjónsson
        Böðvar  Hrafnsson
        ...
        Hugrún  Gunnarsdóttir
        Gils    Hjálmtýsson

    Skipun: 

21. Hversu margir eiga Volvo og búa á Súðavík.
        Svarið ætti að vera 2.
    
    Skipun: 

22. Hvað heita þessir einstaklingar (fornafn), hvernig Volvo eiga þeir?
        Jenný   2012 Volvo XC90
        Embla   2005 Volvo V50

    Skipun: 

23. Hversu mörg mismunandi póstnúmer eru í fakenames skránni?
        Svarið ætti að vera 141 (ath. ekki 142).

    Skipun: 
