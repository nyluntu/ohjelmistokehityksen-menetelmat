# Viite-eheys ja ACID

Tietokannan tärkeimpiä ominaisuuksia on tiedon eheyden ylläpitäminen. Tämä tapahtuu useiden eri toiminnollisuuksien avulla ja on tärkeä asia tietää tietokanta suunnittelun näkökulmasta. Kaikki tietokantaohjelmistot eivät toteuta eheyteen liittyviä ominaisuuksia samalla tavoin, joten on aina hyvä tutustua vieraaseen tietokantaohjelmistoon ensin.

Seuraavassa yhteenvedossa on käsitelty Mysql viite-eheydet sekä ACID -periaatteet mitä niillä tarkoitetaan.

## ACID -periaate

ACID tarkoitetaan joukkoa tietokantajärjestelmien periaatteita ja ominaisuuksia ja lyhenne tulee seuraavista sanoista:

* Atomisuus (Atomicity)
* Eheys (Consistency)
* Eristyneisyys (Isolation)
* Pysyvyys (Durability)

Periaatteiden tarkoituksena on turvata tietokannan tietojen eheys kaikissa tilanteissa. Ominaisuudet ovat käytössä useimmissa tietokantaohjelmistoissa, jotta niitä ei tarvitsisi toteuttaa itse ja sen vuoksi tietokannan käyttäminen oikein on tärkeä huomioida.

Mysql -tietokannan kanssa huomioitavaa on, että **InnoDB** -tietomalli (moottori, storage engine) toteuttaa ACID -periaatteet. MyISAM -ei näitä toteuta, joten tarkista tarvittaessa mitä tapaa tietokannassa käytetään.

### Atomisuus

Tarkoitetaan transaktion suorittamista kokonaan tai ei laisinkaan.

Transaktiolla tarkoitetaan erilaisia tietokantaoperaatioita, jotka on esimerkiksi tarkoitus suorittaa kokonaisuutena.

### Eheys

Tarkoitetaan sitä, että tietokannan tieto on eheää (ehjä, rikkoutumaton).

Kun tietokanta muuttaa tilaansa transaktioiden yhteydessä, huolehtii tietokanta siitä, että tiedon tila on eheä myös lopputilanteessa.

### Eristyneisyys

Tarkoitetaan transaktioiden olevan eristettyjä toisistaan ja toimivat yksinään. Toinen transaktio ei voi siis vaikuttaa toisen suoritukseen.

### Pysyvyys

Tarkoitetaan tiedon pysyvyyttä transaktioiden jälkeen, joka pyritään siihen, että tieto ei katoa enää järjestelmästä.

## Viite-eheys

Viite-eheys toteutetaan viiteavaimilla ja sillä tarkoitetaan sitä, että tietokannan lapsitauluun ei voida merkitä tietoa mitä ei esiinny sen päätaulussa.

Lapsitaulu (child table) on sellainen, jossa on viitevain toiseen tauluun. Tämä toinen taulu on kyseisen taulun päätaulu (parent table) tai monissa lähteissä on käytetty myös termiä "äititaulu".

![Esimerkki pää- ja lapsitauluista.](../.gitbook/assets/screenshot-2019-09-18-at-23.44.10.png)

Yllä olevassa kuvassa on esimerkki pää- ja lapsitauluista. Taulu, joka esiintyy lapsitauluna riippuu aina näkökulmasta ja siitä missä viiteavain esiintyy.

Taulu **televisiosarjat** on _päätaulu_, jos tarkastellaan sen yhteyttä **luojat** tauluun. **Luojat** taulu on siis tässä tilanteessa **televisiosarjat** taulun _lapsitaulu_. Tämä johtuu siitä, että **luojat** taulussa on _viiteavain -kenttä (tvsarja\_id)_, joka viittaa **televisiosarjat** taulun _pääavaimeen (id -kentttä)_.

Kun kyseessä on taas **tyylilajit** taulu niin **televisiosarjat** taulu on _lapsitaulu_ ja tyylilajit on _päätaulu_. Tämä johtuu siitä, että **televisiosarjat** taulussa on _viiteavain -kenttä (tyylilajin\_id)_, joka viittaa **tyylilajit** taulun _pääavaimeen (tyylilajin\_id)_.

Kolmantena esimerkkinä on **televisiosarjat\_tvkanavat** liitostaulu. Tässä tilanteessa kyseinen liitostaulu on _lapsitaulu_ **televisiosarjat** ja **tvkanavat** tauluille. Tällöin **televisiosarjat** ja **tvkanavat** taulut ovat _päätauluja_ liitostaululle.

Näiden välisten yhteyksien huomiointi on tärkeää, koska [viitevainten rajoitussäännöissä](paeae-ja-viiteavaimet.md#rajoitteet) on määritelmiä siitä miten tietokannan taulut tulevat keskenään lopulta toimimaan.

Lue lisää viittaustavoista [ER kaaviot](er-kaaviot.md) yhteenvedosta.

## Lähteet

{% embed url="https://fi.wikipedia.org/wiki/ACID" %}

{% embed url="https://en.wikipedia.org/wiki/ACID" %}

{% embed url="https://en.wikipedia.org/wiki/Atomicity_(database_systems)" %}

{% embed url="https://en.wikipedia.org/wiki/Consistency_(database_systems)" %}

{% embed url="https://en.wikipedia.org/wiki/Isolation_(database_systems)" %}

{% embed url="https://en.wikipedia.org/wiki/Durability_(database_systems)" %}

{% embed url="https://dev.mysql.com/doc/refman/5.7/en/mysql-acid.html" %}

