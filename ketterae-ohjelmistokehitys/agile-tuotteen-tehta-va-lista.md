---
description: Esimerkki tuotteen tehtävälistasta.
---

# Agile, Tuotteen tehtävälista

## Sijainnin merkintä

Yksinkertaisuudessaan tarkoitetaan ohjelmaa, jolla voidaan merkitä sijainti. Sijainti sisältää GPS koordinaatit sekä muita ominaisuuksia, joita ohjelma hyödyntää.

### Käyttäjätarinat

* Koiran ulkoiluttajana tahdon lisätä oman nykyisen sijaintini ulkoilupaikan kartalle, jotta voin ilmoittaa ulkoilupaikasta muille käyttäjille.
* Koiran ulkoiluttajan tahdon nähdä nykyisen sijaintini ympärilläni olevia ulkoilupaikkoja, jotta löydän läheltä sopivan pysähdyspaikan.
* Koiran ulkoiluttajana tahdon tarkastella merkityn ulkoilupaikan tarkempia tietoja, jotta tiedän soveltuuko se koiralleni.
* Koiran ulkoiluttajan tahdon ilmoittaa ulkoilupaikan virheellisestä informaatiosta, jotta tieto olisi ajantasaista.
* Koiran ulkoiluttajan tahdon ilmoittaa väärinmerkityn ulkoilupaikan poistamisesta, jotta tieto olisi ajantasaista.
* Koiran ulkoiluttajan tahdon nähdä sijainnista onko paikalla muita koiran ulkoiluttajia, jotta tiedän onko sijainti sillä hetkellä sopiva koiralleni.
* Koiran ulkoiluttajan tahdon nähdä nykyisen sijaintini ympärilläni olevia yrityksiä, jotka tarjoavat koirille suunnattuja palveluita.
* Koiran ulkoiluttajana tahdon ilmoittaa muille koiranomistajille, että olen menossa valitsemaani sijaintiin tiettynä ajanhetkellä.
* Koiran ulkoiluttajan tahdon lähettää kuvia ulkoilupaikasta valitsemaani sijaintiin.
* Palvelun tarjoajana tahdon, että käyttäjä merkitään sijainnissa olevaksi kun ulkoiluttaja on

  lähellä sijaintia paikkatiedon mukaan.

  Ulkoilupaikkaan liitettäviä tietokenttiä

  • https://gist.github.com/nyluntu/ee674be05a4291ac0a6b8c6d91553603

## Koirien merkintä / lemmikin hallinta

Toiminnon tarkoitus on mahdollistaa käyttäjän lisätä omistamansa lemmikki ohjelmaan. Tässä kohdin lemmikillä tarkoitetaan koiria. Lisättävät tiedot ovat monipuolisia, jotka pitää ottaa huomioon.

### Käyttäjätarinat

* Palvelun tarjoajana, tahdon koiran omistajan pystyvän lisäämään yhden tai useamman koiran tietonsa palveluun.
* Palvelun tarjoajana, tahdon koiran omistajan pystyvän korjaamaan hänen koiran tietonsa palveluun.
* Palvelun tarjoajana tahdon koiran omistajan pystyvät tarkastelemaan oman ja muiden koiranomistajien koirien tietoja.
* Palvelun tarjoajana tahdon koiran omistajien pystyvän voida poistamaan koiransa tiedot palvelusta.
* Koiran omistajana tahdon lisätä yhden tai useamman kuvan koirastani.

  Koiraan liittyviä tietokenttiä

  • https://gist.github.com/nyluntu/c18163689c79a95fd318cdac1cf910f7

## Sijaintien ja lemmikkien seuranta

Toiminnon tarkoitus on mahdollistaa käyttäjien lisätä itselleen seurattavia sijainteja ja lemmikkejä. Puhutaan yleisesti ns. "follow" tyyppisestä toiminnosta, joka on tuttu monesta eri some-palvelusta. Ei ole tarkoitus seurata sijaintia vaan lisätä sijainteja ja lemmikkejä omaan listaan, josta ollaan kiinnostuneita.

### Käyttäjätarinat

* Koiran ulkoiluttajana tahdon pystyä merkitsemään itselleni suosikkisijainteja, jotta löydän ne nopeammin palvelusta.
* Koiran ulkoiluttajana tahdon pystyä näkemään listauksen suosikkisijainneistani.
* Koiran ulkoiluttajana tahdon nähdä suosikkisijainneista, onko paikalla muita koiranomistajia

  kyseisellä ajanhetkellä.

* Koiran ulkoiluttajan tahdon pystyä poistamaan sijainteja suosikkilistaltani.
* Koiran ulkoiluttajana tahdon pystyä merkitsemään muiden omistajien koiria kaverilistalleni,

  jotta löydän tutut koirat nopeammin.

* Koiran ulkoiluttajana tahdon pystyä poistamaan koiria kaverilistaltani.
* Koiran ulkoiluttajan tahdon nähdä kaverilistaani lisäämistä koirista, ovatko ne kyseisellä

  ajanhetkellä ulkoilemassa jossakin sijainnissa.

* Koiran ulkoiluttajan tahdon nähdä kaverilistaani lisäämistä koirista, ovatko ne kyseisellä

  ajanhetkellä ulkoilemassa omistajan kanssa jossakin sijainnissa.

* Koiran ulkoiluttajan tahdon nähdä kaverilistaani lisäämistä koirista, onko omistaja

  ilmoittanut menevänsä ulkoilemaan tiettynä ajanhetkenä johonkin palvelun sisältämissä sijainneista.

