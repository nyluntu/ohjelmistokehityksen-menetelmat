# NUnit perusteet 3

---

Yksikkötestaus ei eroa varsinaisesti ohjelmoinnista ja attribuutit sekä testien kirjoittaminen jää paremmin mieleen ohjelmoimalla.

Sovella aiemmin oppimaasi seuraaviin käytännön läheisiin harjoitustehtäviin. Sinua auttavat myös muutamat apukysymykset.

### Tutustu valmiiseen ohjelmaan, jossa on hyödynnetty testejä

Kloonaa projekti [https://github.com/nyluntu/saliavustaja](https://github.com/nyluntu/saliavustaja)

Käynnistä projekti Visual Studiolla. Yritä kääntää projekti, jotta kaikki riippuvuudet ladataan. Tämän jälkeen valitse projekteista Saliavustaja.UI. Projektin päällä klikkaa hiiren oikeata painiketta ja kontekstimenusta valitse "set as startup project". Tämän jälkeen käynnistä projekti ja kokeile, että ohjelma käynnistyy.

Seuraavaksi sulje ohjelma ja tutustu SaliavustajaTests -projektiin. Yritä saada ajettua testit Visual Studiolla. Yritä tehdä havaintoja testeistä:

* Mitä testit testaavat? Mitä ne siis yrittävät todistaa?
* Miten testiluokat on nimetty?
* Miten testimetodit on nimetty?
* Miten eri attribuutteja on käytetty?
* Miten eri Assert-tarkistuksia on käytetty?
* Miten itse testit on rakenteeltaan ja luettavuudeltaan kirjoitettu?

### Merkkijono laskin -ohjelman toteuttaminen yksikkötestein

Seuraava harjoitus ei ole kirjoittajan oma vaan perustuu Roy Osheroven String Calculator harjoitukseen. [http://osherove.com/tdd-kata-1/](http://osherove.com/tdd-kata-1/)

Vältä katsomasta vastauksia vaan keskity seuraavan tehtävänannon ohjeistukseen ja yritä ratkaista se ensin itse niin pitkälle kuin pääset. Harjoituksen tavoitteena on luoda yksinkertainen ohjelma, joka on tarkoit määritelty ja sen oikea toiminnallisuus tulee todistaa testien avulla.

#### Merkkijono laskin

Tee laskin, joka ottaa numerot String -tyyppisenä vastaan. Ei siis double tai int tai muuna numeromuotona. Luo ohjelma alla mainittujen vaatimuksiin perustuen siten, että sinulla on vähintään yksi testi jokaiselle vaatimukselle. Kun olet kirjoittanut testin, voit vielä tehdä ohjelmasta konsoliohjelman.

Ohjelman tulee toimia siten, että luokan nimi, joka toteuttaa kyseisen vaatimuksen nimi on MerkkijonoLaskin. Luokalla on metodi Laske\(string laskutoimitus\), jolla on yksi string parametri. Kun laskutoimitus on laskettu, palauttaa metodi Int tyyppisen lukuarvon, joka vastaa laskutoimituksen tulosta.

* [ ] Tyhjä merkkinojo palauttaa nollan.
* [ ] Yksi numero, laskin palauttaa annetun numeron arvon..
* [ ] Kaksi numeroa, pilkulla erotettuna, palauttaa lukujen summan.
* [ ] Toteuta ominaisuus, että numeroita voidaan antaa pilkulla erotettuna rajoittamaton määrä ja laskin palauttaa lukujen summan.
* [ ] Toteuta ominaisuus, että pilkkujen tilalla voidaan käyttää newline merkintää lukujen erottimena pilkkujen sijaan. \(newline = \n\)
  * Esimerkiksi arvo "1\n2,3" palauttaisi summan 6.
  * Ei tarvitse tukea muotoa, jossa erottimet seuraavat toisiaan. Esimerkiksi "1,\n". Voidaan olettaa, ettei tällaisia syötteitä anneta.
* [ ] Negatiivinen luku, pienempi kuin nolla, aiheuttaa virheen. \(Exception\)
* [ ] Luvut, jotka ovat yli 1000, ei huomioida yhteenlaskussa.



