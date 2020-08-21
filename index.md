# Knjiga

Poliglot je okolje za učenje programiranja. Programiramo lahko na dva načina, na bločnega ali tekstovnega. Pri programiranju na bločni način so konstrukti predstavleni z bloki, ki jih zlagamo skupaj podobno kot LEGO kocke. Pri tekstovnem načinu pa moramo program napisati v obliki teksta. Bločni način je prjaznejši za začentike saj se pri grajenju programa z bloki ne moremo zatipkati, prav tako pa so nam vsi bloki na voljo v orodjarni tako, da se jih ni potrebno zapomniti na pamet. V industriji se uporabljaja izključno tekstovni način porgramiranja, saj je ta, ko enkrat znamo programirati, dosti hitrejši. Posledično je potrebno po tem, ko se naučimo programiranja v bločnem načinu preiti v tekstovni način. Cilj tega orodja je poenostavi ta prehod.

Programirali bomo v jeziku Limpid, ki je bil posebaj razvit za učenje in ima zato namenoma dosti manj konstruktov, kot ostali jeziki. Kljub temu pa so osnove ne glede na jezik enake, tako da se boste brez težav kasneje naučili še katerega o splošno namenskih jezikov. V nadaljevanju bodo razloženi osnovni konstrukti. Primeri so predstavljeni v obeh načinih, na levi je tekstovna oblika na desni pa bločna.

## Struktura programa

Kaj sploh je programiranje? Programiranje je zapis postopka, ki ga mora računalnik izvesti. Takemu postopku rečemo program. V našem programskem jeziku program zapišemo na naslednji način:

```
program {
}
```

Ta program predstavlja postopek brez enega samega koraka, zato posledično ne naredi ničesar. To je najpreprostejši program, ki ga lahko zapišemo. Takšen porgram ni preveč uporaben, zato mu dodajmo še kakšen ukaz. Dodali bomo ukaz za izpis na zaslon, ki se imenuje ```print```. Zakaj se imenuje print? Ker so prvi računalniki imeli namesto zalona tiskalnik, računalnik je v tistih časih začel dobesedno "printati", ko je dobil ta ukaz. Zraven ukaza print pa je še besedilo, ki ga bo program izpisal na zaslon. V primeru naslednega programa je to ```Zdravo!```:

```
program {
    print "Zdravo!";
}
```

Ta program ima tako en sam korak. Računalnik lahko seveda izvede tudi več korakov zaporedoma. V naslednjem primeru bo izvedel kar tri. Najprej bo izpisal ```Korak 1```, nato ```Korak 2``` in za konec še ```Korak 3```. 

```
program {
    print "To je korak 1";
    print "To je korak 2";
    print "To je korak 3";
}
```

Kot ste opazili je računalnik vsa besedila izpisal kar v eni vrstici. Takšen izpis ne izgleda preveč pregledno. Dajmo vsako besedilo v svojo vrstico! To naredimo tako, da za vsakim besedilom izpišemo še novo vrstico z uporabo ukaza ```line```.

```
program {
    print "To je korak 1";
    print line;
    print "To je korak 2";
    print line;
    print "To je korak 3";
    print line;
}
```

Kot lahko vidite so programi nekakšen kuharski recept za računalnik. Sestavljen je iz večih korakov, ti pa se vedno izvajajo eden za drugim od vrha do dna. Naslednji program izpiše recept za peko palačink! Kot lahko vidimo lahko izpis nove vrstice

```
program {
    print "Vzami posodo." line;
    print "Dodaj jajca." line;
    print "Dodaj moko." line;
    print "Dodaj mleko." line;
    print "Maso vlij v ponev." line;
    print "Speči palačinke!" line;
}
```

## Računske operacije

Besedila niso edina stvar, ki jih zna računalnik izpisati. Razume tudi številke. Na primer naslednji izpiše vaše najljubše število:

```
program {
    print 7;
}
```

Sem uganil? ;) Z števili pa lahko tudi računamo. Na primer računalniku lahko damo za nalogo naj izračuna ```1 + 1```:

```
program {
    print 1 + 1;
}
```

Odgovor je seveda ```2```. Podprte pa so tudi druge računske operacije. Na voljo imamo seštevanje, odštevanje, množenje, deljenje in deljenje celih števil. 

```
program {
    print 1 + 2 line;
    print 1 - 2 line;
    print 1 * 2 line;
    print 1 / 2 line;
    print 1 // 2 line;
}
```


Računalnik je torej kot neke vrste kalukator. Lahko izračuna poljubne račune, za razliko od kalukatorja pa lahko izračuna zaporedoma več računov ne le enega. Opazite lahko, da je računalnik pri zadnjem izračunu vrnil ```0```. V primeru, da želimo da je rezultat deljenja celo število mora računalnik rezultat zaokroži navzdol. To pomeni da preprosto odstrani del za decimalno vejico, na primer ```1.3``` se zaokroži na ```1```, ```1.5``` se prav tako zaokroži na ```1```, ```7.6``` se zaokroži na ```7```, ```9.9``` se zaokorži na ```9```. Seveda pa računalnik lahko računa tudi z večjimi števili. Brez težav opravi z naslednjimi računi za katere bi mi že potrebovali kalkulator:

```
program {
    print 502 + 78 line;
    print 78858 - 4485 line;
    print 1147 * 99 line;
    print 77888 / 222 line;
}
```

## Spremenljivke

Računalnik ima tudi spomin kamor lahko shranimo števila. Mesto kamor si je računalnik število shranil moramo nekako označiti, da bomo število lahko kasneje dobili nazaj. To storimo tako da mu mestu dodelimo ime, lahko je karkoli, vendar je najbolje da izbiramo imena, ki nas spomnijo kaj smo tja shranili. Temu imenu rečemo spremenljivka. Na primer:

```
program {
    x: 1;
}
```

Ta program na mesto ```x``` shrani število ```1```. Če program poženemo bomo opazili, da se na videz ni zgodilo nič. Zakaj? Računalniku smo naročili naj samo shrani število v spomin, ta ukaz ne izpiše ničesar na zaslon. Za izpis imamo ukaz ```print```. Če želimo pogledati kaj ima računalnik zapisano na mestu ```x``` lahko to storimo tako, da vrednost preprosto izpišemo na zaslon:

```
program {
    x: 1;
    print x;
}
```

Ta progam si najprej število shrani, nato pa ga izpiše na zaslon. Vedno, ko nas zanima kaj ima računalnik shranjeno v spominu na določeni točki v programu lahko vrednost vedno izpišemo na zaslon in pogledamo.

Poleg števil samih pa lahko shranimo v spremenljivko tudi rezultat matematičnega izraza. Tako lahko dele izračuna ponovno uporabimo.
```
program {
    x: 10 * (99 - 0.5);
    y: 7 * x;
    print "x = " x line;
    print "y = " y line;
}
```

Kot uporaben primer lahko vzamemo pretvornik enot. Kot že veste naš merski sistem temelji na večkratnikih števila dest, npr. metre lahko v kilometre pretvorimo tako da delimo z ```10^3```. V Ameriki so ohranili dokaj nenavaden sistem, ker med sosednjimi enotami ni nekega smiselnega razmerja. Za merjenje razdalje uporabljajo kot osnovno enoto korak, ki je nekje tretina metra, nato pa sta iz nje izpeljani npr. inč, ki je dvanajstina koraka in milja, ki je točno 5280 korakov. Sto metrov lahko v različne enote pretvorimo s spodnjim programom, razmerja med enotami lahko izračunamo v naprej in jih shranimo v spremenljivke.

```
program {
    kilo: 1000;
    foot: 0.3048;
    mile: 5280 * foot;
    inch: foot / 12;
    
    n: 100;
    print n " m" line;
    print n / kilo " km" line;
    print n / foot " ft" line;
    print n / mile " mi" line;
    print n / inch " in" line;
}
```

Vrednost spremenljivke pa lahko tudi *spremenimo*, torej ji dodelimo neko drugo vrednost. V spodnjem programu je vrednost ```x``` najprej ```1```, nato pa jo spremenimo na ```2```.

```
program {
    x: 1;
    print x line;
    x: 2;
    print x line;
}
```

V izrazu lahko uporabimo tudi spremenljivko samo, torej uporabimo njeno prejšnjo vrednost. Na takšen način lahko implementirano števec:

```
program {
    x: 0;
    print x line;
    x: x + 1;
    print x line;
    x: x + 1;
    print x line;
    x: x + 1;
    print x line;
    x: x + 1;
    print x line;
}
```

## Vhod in izhod

Do sedaj smo vrednosti samo izpisovali, lahko pa jih tudi preberemo. Na takšen način uporabniku našega programa omogočimo da v program vstavi svojo vrednost.
Najpreprostejši tak program prebere vrednost in jo tako izpiše na zaslon:

```
program {
    x: input;
    print x;
}
```

Tak program lahko nato nadgradimo, tako da izpišemo še predhodnika in naslednjika števila.

```
program {
    x: input;
    print "Predhodnik: " x - 1 line;
    print "Število: " x line;
    print "Naslednik: " x + 1 line;   
}
```

Na podoben način lahko nadgradimo tudi naš pretvornik enot, tako da lahko uporabnik sam vnese število:

```
program {
    kilo: 1000;
    foot: 0.3048;
    mile: 5280 * foot;
    inch: foot / 12;
    
    n: input;
    print n " m" line;
    print n / kilo " km" line;
    print n / foot " ft" line;
    print n / mile " mi" line;
    print n / inch " in" line;
}
```

Uporabinik lahko seveda vnese tudi več števil, naslednji program prebere dve števili in izpiše njuno vsoto:

```
program {
    x: input;
    y: input;
    print x + y;
}
```

## Vejitve
Vejitve nam omogočajo, da se lahko računalnik odloči kaj bo storil, glede na to ali je nek pogoj resničen ali ne-resničen. Vejitve predstavimo s trditvijo ```if```. Kot preprost pogoj vzamimo ```x``` je enako nič (```x = 0```). Računalnik pri spodnjem programu izpiše sporočilo samo, *če* je pogoj resničen. Z drugimi besedami telo trditve ```if``` (ukazi med ```{``` in ```}```) se izvedejo le *če* je pogoj resničen, drugače se ne zgodi nič.

```
program {
    x: input;
    if (x = 0) {
        print "x je nič!"; 
    }
}
```

Če želimo, da program nekaj izpiše v primeru da zgoren pogoj *ni* resničen to storimo da dodamo še trditev ```else``` (ki pomeni sicer):

```
program {
    x: input;
    if (x = 0) {
        print "x je nič!"; 
    }
    else {
        print "x ni nič :("; 
    }
}
```

### Logični operatorji
Logični operatorji nam omogočajo, da različne trditve kombiniramo. Osnovi trije so konjunkcija (```and```), disjunkcija (```or```) in negacija (```not```). Ti operatorji so podobni klasičnim matematičnim operacijam (seštevanje, množenje), ki jih že poznamo, razlikujejo se v tem, da delujejo nad logočnimi vrednostmi, ki sta *res* in *ni res*.

#### Konjunkcija
Operator nam omogoča da preverimo ali sta hkrati resnična oba pogoja, torej če je resničen prvi pogoj *in* če je hkrati resničen drugi pogoj. Npr. če želimo, da program nekaj izpiše v primeru, da je vrednost med nekima dvema vrednostima, lahko najprej preverimo če je naša vrednost hkrati večja od prve *in* manjša od druge. Pri spodnjem programu pogoj preberemo kot "če je vrednost večja od ```5``` in če je vrednost manjša od ```10```", kar pomeni da je med ```5``` in ```10```: 

```
program {
    x: input;
    if (5 <= x and x <= 10) {
        print "x je med 5 in 10"; 
    }
}
```

Na operator ```and``` lahko gledamo tudi kot na presek množic. Množica vseh števil večjih od ```5``` je enaka ```{5, 6, 7, 8, 9, 10, 11, ...}``` in množica vseh števil manjših od ```10``` je enaka ```{..., 1, 2, 3, 4, 5, 6, 7, 8, 9, 10}```, torej je njun presek je ravno ```{5, 6, 7, 8, 9, 10}```. Spročilo izpiše le če je naše število eno od prej naštetih.

#### Disjunkcija
Operator nam omogoča, da preverimo ali je resničen prvi *ali* drugi pogoj. Npr. če želimo preveriti ali je vrednost enaka ```1``` *ali* ```2``` lahko to storimo tako:

```
program {
    x: input;
    if (x = 1 or x = 2) {
        print "x je enak 1 ali 2"; 
    }
}
```

Iz vidika množic operator ```or``` predstavlja unijo. Množica števil, ki so enaka ```1``` je ```{1}``` in množica števil, ki so enaka ```2``` je ```{2}```, torej je njuna unija ```{1, 2}```, program bo nekaj izpisal le, če je naše število eno od naštetih tako kot prej.

#### Negacija
Tretja operacija je operacija ```not```, ki vrednost pogoja obrne, torej če je bil pogoj resničen ta postane ne-resničen in obratno. Z operacijo ```not``` lahko nadomestimo trditev ```else```:

```
program {
    x: input;
    if (x = 0) {
        print "x je nič!"; 
    }
    if (not (x = 0)) {
        print "x ni nič :("; 
    }
}
```

Oz. izpišemo nekaj le če število ni enako nič:

```
program {
    x: input;
    if (not (x = 0)) {
        print "x ni nič!"; 
    }
}
```

Iz vidika množic operacija ```not``` predstavlja kompliment, torej množico vseh števil ki so enake ```0```, ```{0}```,  spremeni v ```{..., -2, -1, 1, 2, ...}```, torej v množico vseh števil, razen ```0```.

### Veriženje

Več pogojnih trditev lahko verižimo eno za drugo. Torej če želimo preveriti ali je število pozitivno, negativno ali nič (ki ni ne negativno in ne pozitivno) lahko to storimo takole:

```
program {
    x: input;
    if (x < 0) {
        print "x je negativen"; 
    }
    else if (x > 0) {
        print "x je pozitiven"; 
    }
    else {
        print "x je enak nič"; 
    }
}
```
Torej če imamo množico celih števil ```{..., -2, -1, 0, 1, 2, ...}``` prvi pogoj zajame vrednosti, ki so manjše od nič (negativne), ```{..., -2, -1}```, ostane nam ```{0, 1, 2, ...}```. Drugi pogoj zajame vrednosti večje od nič (pozitivne) ```{ 1, 2, ...}```. Na koncu pa nam ostane še samo ```{0}```, torej nič.

Zgoren program je kraša oblika tega, kombinirana trditev ```else if``` nam omogoča, da se izognemu gnezednju.

```
program {
    x: input;
    if (x < 0) {
        print "x je negativen"; 
    }
    else {
        if (x > 0) {
            print "x je pozitiven"; 
        }
        else {
            print "x je enak nič"; 
        }
    }
}
```

Z uporabo logičnih operatorjev bi lahko zgoren program zapisali tudi tako:

```
program {
    x: input;
    if (x < 0) {
        print "x je negativen"; 
    }
    if (not (x < 0) and x > 0) {
        print "x je pozitiven"; 
    }
    if ((not (x < 0)) and (not (x > 0))) {
        print "x je enak nič";
    }
}
```

## Zanke
Zanke so podobne vejitvam, le da se trditev izvaja dokler je pogoj resničen. Predstavimo jih s trditvijo ```while```. Vzamimo prvi primer iz prejšnjega poglavja in zamenjajmo ```if``` z ```while```.

```
program {
    x: input;
    while (x = 0) {
        print "x je nič!"; 
    }
}
```

Kot lahko vidimo v primeru, da vnesemo število ```0``` se telo zanke izvede neskončno krat v nasprotnem primeru pa se ne zgodi nič. Program, ki samo izpisuje neko sporočilo v neskončnost ni preveč uporaben. Spomnimo se, da lahko vrednost spremenljivke spremenimo, torej lahko dosežemo, da se zanka enkrat zaključi:

```
program {
    print "x = ";
    x: input;
    while (x = 0) {
        print "x je nič!" line;
        print "x = ";
        x: input;
    }
}
```

Na tak način lahko implementiramo program za ugibanje najljubšega števila:

```
program {
    n: 7;
    print "x = ";
    x: input;
    while (x /= n) {
        print "narobe!" line;
        print "x = ";
        x: input;
    }
    print "uganil!" line;
}
```

V poglavju spremnljivke smo predstavili števec, kaj se zgodi če ga uporabimo v zanki? Program izpiše vsa števila od ```0``` do ```10```.
 
```
program {
    x: 0;
    while (x <= 10) {
        print x line;
        x: x + 1;
    }
}
```

Vsa števila od ```0``` do ```10``` lahko tudi seštejemo na podoben način, le da sedaj prištevamo ```x``` namesto ```1```. 
 
```
program {
    x: 0;
    vsota: 0;
    while (x <= 10) {
        print x line;
        x: x + 1;
        vsota: vsota + x;
    }
    print "Vsota: " vsota line;
}
```

## Kam naprej?
Naš jezik je seveda preveč omejen za razvoj večjih aplikacij. Pot lahko nadaljujete, tako da se naučite še kakšnega drugega jezika. Kot boste videli je povsod začetni del popolmoma enak temu kar ste se ravnokar naučili.

- [Python](https://docs.python.org/3/tutorial/)
- [Haskell](http://learnyouahaskell.com/chapters)
- [Scheme](http://www.shido.info/lisp/idx_scm_e.html)
- [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
