---
description: UML (Unified Modeling Language) -kaavioiden perusteet.
---

# Johdanto

UML on lyhenne termeistä Unified Modelin Language. Kyseessä on tapa mallintaa ohjelmiston komponentteja, rakenteita ja suoritusvaiheita. UML sisältää useita erilaisia kaaviotyyppejä mallintamiseen ja antaa täten valmiita, sekä standardoituja tapoja, kuvata ohjelmistojen suunnitteluun liittyviä asioita.

Historia ulottuu 80-luvun lopulle mutta ensimmäinen UML 1.0 julkaistiin vuonna 1997. Voidaan ajatella tämän olevan lähtökohta UML -mallinnuskielelle. Kyseessä on siis mallinnuskieli, ei menetelmä. Kuvaustapoja on olemassa erilaisia ja mikään ei ole varsinaisesti väärin. UML on yksi tunnetuimpia tapoja ja täten tarjoaa yhtenäisen tavan kuvata ja suunnitella ohjelmistoja.

Artikkelissa tuon esille asioita mitkä ovat hyvä tuntea ohjelmoijan näkökulmasta. Moni asia perustuu lähteissä mainittuihin teoksiin tai Internet lähteisiin. Kaikkia eri kaaviotyyppejä ei käsitellä vaan esille nostetaan niitä, jotka kirjoittaja on kokenut toimivammaksi.

On hyvä muistaa, että UML ei kovin usein tule tänä päivänä ilmi. Ketterän ohjelmistokehityksen toimintamallit ovat muuttaneet työtapoja ja moni ennestään olemassa oleva asia unohtuu. UML historia on kuitenkin hyvin paljon olio-ohjelmoinnin suosion alkupäässä ja sisältää paljon oliokeskeisiä mallinnustapoja. Ohjelmistokehityksessä on usein suunnitteluun ja analyysiin keskittyvä vaihe missä tehdään etukäteen suunnitelmia ohjelmiston rakenteesta. Näihin tilanteisiin UML -mallinnuskieli on tehty.

Vaikka ohjelmistojen tuottaminen on muuttunut 80- ja 90-luvusta lähtien valtavasti, sekä myös 2000 -luvun alusta niin UML -mallinnuskielelle on silti paikka ohjelmistokehityksessä. Tänä päivänä suositaan lyhyempiä suunnitteluvaiheita ja keskittymistä toteutusvaiheeseen. UML -kuitenkin tarjoaa hyvän "kirjaston" erilaisia mallinnustapoja, jotka auttava ajatusten hahmottamisessa ja viestimisessä.

Dokumentointi on tärkeässä osassa ohjelmistotuotantoa. Dokumentoinnin haasteet ovat lähinnä nopeasti muuttuvissa vaatimuksisa ja vaarana sen vanheneminen. UML -kaavioita käsin piirtäen ei ole tehokkain dokumentointitapa muuttuvien vaatimusten vuoksi. Mukaan on tullut paljon kaavioiden piirtämiseen tarkoitettuja ohjelmistoja sekä työkaluja, jotka luovat olemassa olevasta lähdekoodista halutunlaisia kaavioita.

Aloitetaan tutustuminen muutamiin tärkeimpiin kaaviotyyppeihin. Sen kautta pyrimme tutustumaan miten UML -mallinnuskielestä voi olla hyötyä ohjelmistoja suunnitellessa.

## Kaaviotyypit

UML -mallinnuskieli sisältää useita kaaviotyyppejä ja ne voidaan karkeasti jakaa kolmeen erilaiseen päätyyppiin.&#x20;

**Rakennekaavio (Structure diagram)**

* Komponenttikaavio (Component diagram)
* Koostekaavio (Composite structure diagram)
* _<mark style="background-color:green;">Luokkakaavio</mark>_ (Class diagram)
* Oliokaavio (Object diagram)
* Pakkauskaavio (Package diagram)
* Sijoittelukaavio (Deployment diagram)

**Käyttäytymiskaavio (Behavior diagram)**

* _<mark style="background-color:green;">Aktiviteettikaavio</mark>_ (Activity diagram)
* _<mark style="background-color:green;">Käyttötapauskaavio</mark>_ (Use case diagram)
* Tilakaavio (State (machine) diagram)

**Vuorovaikutuskaavio (Interaction diagram)**

* Ajoituskaavio (Timing diagram)
* Kokoava vuorovaikutuskaavio (Interaction overview diagram)
* Kommunikointikaavio (Communication diagram)
* Sekvenssikaavio (Sequence diagram)

Kaaviot voidaan karkeasti jakaa kolmeen erilaiseen päätyyppiin.&#x20;

_Rakennekaaviot_ kuvaavat ohjelmiston rakenteita, joiden täytyy olla mallinnettavassa järjestelmässä. Tämä voi tarkoittaa esimerkiksi ohjelmiston eri komponenttien osittamista toisiinsa nähden.&#x20;

![Esimerkki luokkakaaviosta](<../.gitbook/assets/luokkakaavio esimerkki.png>)

_Käyttäytymiskaaviot ****_ korostavat ohjelmsiton käyttäytymistä eri tilanteissa. Esimerkiksi miten ohjelman logiikan tulisi toimia kuvatussa tilanteessa.&#x20;

![Esimerkki aktiviteettikaaviosta](<../.gitbook/assets/esimerkki aktiviteettikaaviosta.png>)

_Vuorovaikutuskaaviot_ korostavat yksittäisten ohjelmiston osien yhteistyötä. Esimerkiksi voidaan kuvata kahden eri järjestelmän välistä viestimistä ja käyttäytymistä.

![Esimerkki sekvenssikaaviosta](<../.gitbook/assets/sekvenssikaavio esimerkki.png>)

### Kuvauskieli

UML -kaaviot sisältävät standardoidun kuvauskielen eli notaation. Kirjallisuudessa puhutaan siis notaatiosta millä tarkoitetaan eri kaavioille luotuja merkintätapoja. Yhteenveto näistä notaatioista löytyy alla olevasta liitetiedostosta.

{% file src="../.gitbook/assets/uml notaatiot.pdf" %}
Tiedosto sisältää lähdeteoksesta skannatun yhteenvedon notaatioista.
{% endfile %}

Tutustu myös Tutorials Point sivuston notaatioiden yhteenvetoon.

{% embed url="https://www.tutorialspoint.com/uml/uml_basic_notations.htm" %}

### Luokkakaaviot

Luokkakaavioista on tullut oliosuuntautuneiden menetelmien keskeinen osa. Näihin liittyy erittäin laaja joukko mallinnuskäsitteitä. Materiaalissa esittellään ns. peruskäsitteet, joita tarvitaan useammin.

Luokkakaavio tarkoitus on kuvata järjestelmässä olevia oliotyyppejä ja niiden välillä esiintyviä erilaisia staattisia suhteita. Nämä suhteet jakautuvat kahteen päätyppiin:

* Assosisaatiot - esimerkiksi asiakas voi vuokrata joukon videoita.
* Alityypit - sairaanhoitaja on yksi henkilölaji.

Suhteiden lisäksi luokkakaavioissa voidaan esittää **operaatioita**, jotka ovat niitä prosesseja mitkä luokka osaa toteuttaa. Tällainen voi olla luokkakaavion esimerkissä oleva Tilaus-luokan **lähetä()**-operaatio.

{% file src="../.gitbook/assets/uml luokkakaavio esimerkki.pdf" %}

Tutustu myös Tutorials Point sivuston tarjoamaan materiaaliin luokkakaavioihin liittyen.

{% embed url="https://www.tutorialspoint.com/uml/uml_class_diagram.htm" %}

{% embed url="https://fi.wikipedia.org/wiki/Luokkakaavio" %}

### Aktiviteettikaaviot

Aktiviteettikaavioita käytetään järjestelmän työkulun mallintamiseen. Toiselta nimeltä nämä tunnetaan myös _toimintakaavioina_. Toimintakaavio kuvaa tehtävien tapahtumajärjestystä. Siinä voidaan esitellä ehdollista, että rinnakkaista toimintaa. Aktiviteettikaaivo muistuttaa _tilakaaviota_ mutta niiden sisällössä on pieniä eroja. Notaatiot muistuttavat toisiaan.

{% file src="../.gitbook/assets/uml aktiviteettikaavio esimerkki.pdf" %}

Tutustu myös Tutorials Point sivuston yhteenvetoon aktiviteettikaavioista.

{% embed url="https://www.tutorialspoint.com/uml/uml_activity_diagram.htm" %}

{% embed url="https://fi.wikipedia.org/wiki/Aktiviteettikaavio" %}

### Käyttötapauskaaviot

Käyttötapaukset (use cases) ovat tapa kuvata järjestelmän ominaisuuksia sekä niiden tavoitteita. Nämä ovat usein tekstipohjaisia kevyitä kuvauksia siitä miten järjestelmän tulisi toimia tietyssä tissa. Käyttötapauksista on puhuttu erikseen tämän sivuston [materiaaleissa](../ketterae-ohjelmistokehitys/agile-kaeyttaejaetarina-ja-kaeyttoetapaus.md#kaeyttoetapaus).&#x20;

Käyttötapauskaaviot puolestaan ovat tapa mallintaa näitä vaatimuksia suhteellisen yksinkertaisella tavalla. Kaavioihin liittyy lähinnä **toimijoiden, käyttötapausten** ja niiden välisten **suhteiden** kuvaamista.

{% file src="../.gitbook/assets/uml kayttotapauskaavio esimerkki.pdf" %}

Tutustu myös Tutorials Point sivuston yhteenvetoon käyttötapauskaavioista.

{% embed url="https://www.tutorialspoint.com/uml/uml_use_case_diagram.htm" %}

{% embed url="https://fi.wikipedia.org/wiki/K%C3%A4ytt%C3%B6tapauskaavio" %}

## Lähteet

UML, Martin Fowler & Kendal Scott, Docendo, 2. painos 2004 (alkuperäinen teos Martin Fowler, Kendal Scott: UML Distilled, [https://www.pearson.com/uk/educators/higher-education-educators/program/Fowler-UML-Distilled-A-Brief-Guide-to-the-Standard-Object-Modeling-Language-2nd-Edition/PGM454835.html](https://www.pearson.com/uk/educators/higher-education-educators/program/Fowler-UML-Distilled-A-Brief-Guide-to-the-Standard-Object-Modeling-Language-2nd-Edition/PGM454835.html))

Wikipedia, Unified Modeling Language, [https://en.wikipedia.org/wiki/Unified\_Modeling\_Language](https://en.wikipedia.org/wiki/Unified\_Modeling\_Language)

Wikipedia, UML -mallinnus, [https://fi.wikipedia.org/wiki/UML-mallinnus](https://fi.wikipedia.org/wiki/UML-mallinnus)





