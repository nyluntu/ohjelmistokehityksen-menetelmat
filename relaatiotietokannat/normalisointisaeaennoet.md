---
description: >-
  Luvussa käsitellään tietokantojen normalisointisääntöjä, jotka tulisi tuntea
  tietokantasuunnittelun vuoksi. Normalisointisäännöt ohjaavat kohti hyvää
  tietokantaratkaisua.
---

# Normalisointi

## Mitä normalisoinnilla tarkoitetaan?

Lyhyesti sanottuna normalisointi \(eng. normalization\) tarkoittaa tietokantasuunnitteluun liittyviä tekniikoita, joiden tarkoitus on minimoida tiedon toistuvuutta ja riippuvuutta. Säännöt keskittyvät oleellisesti tietokantataulujen sisältöihin.

Noudattamalla sääntöjä ne ohjaavat siihen, että suuri taulu saadaan pilkottua pienemmiksi tauluiksi sekä luomaan näiden välille riippuvuussuhteita. Kts. [Pää- ja viiteavaimet](paeae-ja-viiteavaimet.md). Lopputuloksena tietokannassa oleva tieto on siis selkeämmin järjestetty. Terminä normalisointi viittaakin tietokannan rakenteisiin . 

Erilaisia normaalimuotoja on yhteensä kuusi kappaletta mutta pääasiassa kolme ensimmäistä on tärkeintä. Kolmannen jälkeen ei aina saada suuria hyötyjä mutta hyvä tapa on yrittää noudattaa kolmea ensimmäistä. Sääntöjen noudattaminen tarkoittaa myös, että toteuttaakseen esimerkiksi kolmannen normaalimuodon pitää sen hetkisen ratkaisun toteuttaa myös kaksi edellistä normaalimuotoa.

Kun tietokannassa on huomioitu nämä säännöt niin voidaan lyhyesti aina ilmaista esimerkiksi, että tietokantamalli on 3. normaalimuodon mukainen. Tämä jo heti antaa viitteen sille minkälainen tietokanta on kyseessä. Aina näin ei ole ja suunnitteluvirheet johtavat erilaisiin ongelmiin tiedon käsittelyn kanssa.

Normalisoinnin lisäksi voidaan puhua denormalisoinnista \(eng. denormalization\), joka tarkoittaa sääntöjen rikkomista. Tämä tehdään usein hyvästä syystä ja perustellen. Ei siksi, että sääntöjä ei noudatettaisi vaan sillä voidaan joissain tilanteissa nostaa esimerkiksi suorituskykyä.

Tutustutaan seuraavaksi kolmeen ensimmäiseen normaalimuotoon syvemmin.

## Normalisoimaton tieto

Normalisointisäännöt tullaan esittämään esimerkin kautta. Ensimmäisenä esittelemme  normalisoimattoman taulun, josta esimerkit syntyvät. Tietokantamalli ei voi toteuttaa seuraavaa normaalimuotoa ellei se toteuta myös edellisiä normaalimuotoja.

On mahdollista, että oikean tiedon kanssa tietyissä olosuhteissa normalisointisäännöt eivät toteudu tai ne niiden yli voidaan hypätä. Esimerkki on kuitenkin tehty siitä näkökulmasta, että erilaiset tilanteet tulevat vastaan. Tietokantamallina toimii seuraavanlainen tv-sarjoja sisältävä tietokantataulu.

![Normalisoimaton tietokantataulu](../.gitbook/assets/screenshot-2019-09-17-at-17.09.02.png)

Kun tietoa ei ole tallennettu oikealla tavalla, tuottaa se usein ongelmia. Tiedon lisääminen, muokkaaminen ja poistaminen osoittautuu yleensä hankalaksi. Seuraavia normaalimuotoja sovelletaan esimerkin tauluun.

## Ensimmäinen normaalimuoto \(1NF\)

Kirjoita: Sarake ei saisi sisältää useita arvoja.

## Toinen normaalimuoto \(2NF\)

Kirjoita: Rivin sarakkeiden arvojen tulee olla riippuvaisia vain rivin pääavaimesta.

## Kolmas normaalimuoto \(3NF\)

Kirjoita: sarakkeiden säännöt eivät saisi riippua toisistaan, nämä tulee siirtää erilliseen tauluun.

## Muut normaalimuodot \(4NF,5NF,6NF\)

Kirjoita:

## Poikkeustilanteiden huomiointi

Kirjoita:



## Lähteet

{% embed url="https://www.w3schools.in/dbms/database-normalization/" %}

{% embed url="https://en.wikipedia.org/wiki/Database\_normalization" %}



