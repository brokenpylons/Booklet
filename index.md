# Knjiga

Poliglot je okolje za učenje programiranja. Programiramo lahko na dva načina, na bločnega ali tekstovnega. Pri programiranju na bločni način so konstrukti predstavleni z bloki, ki jih zlagamo skupaj podobno kot LEGO kocke. Pri tekstovnem načinu pa moramo program napisati v obliki teksta. Bločni način je prjaznejši za začentike saj se pri grajenju programa z bloki ne moremo zatipkati, prav tako pa so nam vsi bloki na voljo v orodjarni tako, da se jih ni potrebno zapomniti na pamet. V industriji se uporabljaja izključno tekstovni način porgramiranja, saj je ta, ko enkrat znamo programirati, dosti hitrejši. Posledično je potrebno po tem, ko se naučimo programiranja v bločnem načinu preiti v tekstovni način. Cilj tega orodja je poenostavi ta prehod.

Programirali bomo v jeziku Limpid, ki je bil posebaj razvit za učenje in ima zato namenoma dosti manj konstruktov, kot ostali jeziki. Kljub temu pa so osnove ne glede na jezik enake, tako da se boste brez težav kasneje naučili še katerega o splošno namenskih jezikov. V nadaljevanju bodo razloženi osnovni konstrukti. Primeri so predstavljeni v obeh načinih, na levi je tekstovna oblika na desni pa bločna.

## Struktura programa

Kaj sploh je programiranje? Programiranje je zapis postopka, ki ga mora računalnik izvesti. Takemu postopku rečemo program. V našem programskem jeziku program zapišemo na naslednji način:

```
program {
}
```

Ta program predstavlja postopek brez enega samega koraka, zato posledično ne naredi ničesar. To je najpreprostejši program, ki ga lahko zapišemo. Takšen porgram ni preveč uporaben, zato mu dodajmo še kakšen ukaz. Dodali bomo ukaz za izpis na zaslon, ki se imenuje ```print```. Zakaj se imenuje print? Ker so prvi računalniki imeli namesto zalona tiskalnik, računalnik je v tistih časih začel dobesedno "printati", ko je dobil ta ukaz. To ime je torej izbrano zgolj iz konvencije. Zraven ukaza print pa je še besedilo, ki ga bo program izpisal na zaslon. V primeru naslednega programa je to ```Zdravo!```:

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

Kot ste opazili je računalnik vsa besedila izpisal kar v eni vrstici. Takšen izpis ne izgleda preveč pregledno. Dajmo vsako besedilo v svojo vrstico! To naredimo tako, da za vsakim besedilom izpišemo še znak za novo vrstico. Tega predstavlja besedica ```line```.

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

Kot lahko vidite so programi nekakšen kuharski recept za računalnik. Sestavljen je iz večih korakov, ti pa se vedno izvajajo eden za drugim od vrha do dna. Naslednji program izpiše recept za peko palačink!

```
program {
    print "Vzami posodo.";
    print line;
    print "Dodaj jajca.";
    print line;
    print "Dodaj moko.";
    print line;
    print "Dodaj mleko.";
    print line;
    print "Maso vlij v ponev.";
    print line;
    print "Speči palačinke!";
    print line;
}
```

## Računske operacije

Besedila niso edina stvar, ki jih zna računalnik izpisati. Razume tudi številke. Na primer naslednji izpiše vaše najljubše število:

```
program {
    print 7;
}
```

Sem uganil? ;) Podprta so samo cela števila. Torej računalnik števila ```1.4``` ne bo razumel. Z števili pa lahko tudi računamo. Na primer računalniku lahko damo za nalogo naj izračuna ```1 + 1```:

```
program {
    print 1 + 1;
}
```

Odgovor je seveda ```2```. Podprte pa so tudi druge računske operacije. Na voljo imamo seštevanje, odštevanje, deljenje in množenje. 

```
program {
    print 1 + 2;
    print 1 - 2;
    print 1 * 2;
    print 1 / 2;
}
```


Računalnik je torej kot neke vrste kalukator. Lahko izračuna poljubne račune, za razliko od kalukatorja pa lahko izračuna zaporedoma več računov ne le enega. Opazite lahko, da je računalnik pri zadnjem izračunu vrnil ```0```. Se je morda zmotil? Kot sem že omenil so podprta samo cela števila, zato v primeru kot števili nista deljivi računalnik rezultat zaokroži navzdol. To pomeni da preprosto odstranimo del za decimalno vejico, na primer ```1.3``` se zaokroži na ```1```, ```1.5``` se prav tako zaokroži na ```1```, ```7.6``` se zaokroži na ```7```, ```9.9``` se zaokorži na ```9```. Seveda pa računalnik lahko računa tudi z večjimi števili. Brez težav opravi z naslednjimi računi za katere bi mi že potrebovali kalkulator:

```
program {
    print 502 + 78;
    print 78858 - 4485;
    print 1147 * 99;
    print 77888 / 222;
}
```

## Spremenljivke

Računalnik ima tudi spomin kamor lahko shranimo števila. Mesto kamor si je računalnik število shranil moramo nekako označiti, da bomo število lahko kasneje dobili nazaj. To storimo tako da mu mestu dodelimo ime, lahko je karkoli, vendar je najbolje da izbiramo imena, ki nas spomnijo kaj smo tja shranili. Na primer:

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


## Vhod in izhod


## Pogoji


## Zanke


## Kam naprej?
