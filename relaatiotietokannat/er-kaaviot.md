---
description: >-
  Luvussa käsitellään Entity Relationship -kaavioita. Lyhennettynä ER tai ERD
  riippuen lähteistä. Niiden tarkoitus on olla apuna tietokannan suunnittelussa
  sekä kommunikoinnissa.
---

# ER kaaviot

## Kaavioiden tarkoitus

Kerro mitä hyötyjä näistä on.

## Termistön läpikäynti

**Entiteetti \(eng. entity\)** - tarkoittaa ... 

**Attribuutti \(eng. attribute\)** - tarkoittaa ... 

**Suhde \(eng. relationship\)** - tarkoittaa ...

## Taulujen väliset suhteet

Tietokantoja suunnitellessa on tärkeää tuntea taulujen väliset suhteet ja niiden kuvaustavat. Kyseessä ei ole sen erityisempi asia kuin, että tarkoitus on kuvata tietokannan sisältämän tiedon keskinäisiä suhteita. Esimerkiksi, jos opiskelija voi osallistua useammalle kurssille, voidaan tällöin sanoa, että opiskelijan ja kurssin välillä on eräänlainen suhde mikäli se mallinnetaan tietokannaksi. Näitä suhteita siis löytyy arkielämästä asioista, joita tietokanta sisältää.

Tietojen välillä voi olla seuraavia suhteita:

* Yksi suhde yhteen \(eng. One-to-One\)
* Yksi suhde moneen \(eng. One-to-Many\)
* Moni suhde yhteen \(eng. Many to One\)
* Moni suhde moneen \(eng. Many-to-Many\)

**Yksi suhde yhteen** - tarkoittaa sellaista suhdetta kahden asian välillä, joita voi olla olemassa vain yksi kerrallaan. Esimerkkinä voisimme ajatella autovuokraamoa. On sovittu, että vuokraajalla voi olla vain yksi auto vuokralla kerrallaan ja auto voi olla vain yhdellä vuokraajalla. Voisimme esittää suhteen seuraavalla kaaviolla.

![](../.gitbook/assets/one-to-one-crows.png)

**Yksi suhde moneen** - tarkoittaa ...

**Moni suhde yhteen** - tarkoittaa ...

**Moni suhde moneen** - tarkoittaa ...

## Taulujen väliset suhteet SQL kielellä

Esimerkit miten nämä tehdään oikeasti SQL tietokannassa.

## Muita notaatioita

Esittele Crow's foot

Esittele UML

{% embed url="https://en.wikipedia.org/wiki/Entity%E2%80%93relationship\_model\#Cardinalities" %}

## Lähteet

{% embed url="https://www.guru99.com/er-diagram-tutorial-dbms.html" %}



