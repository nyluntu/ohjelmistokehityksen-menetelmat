# NUnit perusteet 103



Yksikkötestaus ei eroa varsinaisesti ohjelmoinnista ja attribuutit sekä testien kirjoittaminen jää paremmin mieleen ohjelmoimalla.

Sovella aiemmin oppimaasi seuraaviin käytännön läheisiin harjoitustehtäviin. Sinua auttavat myös muutamat apukysymykset.

#### Tutustu valmiiseen ohjelmaan, jossa on hyödynnetty testejä {#tutustu-valmiiseen-ohjelmaan-jossa-on-hy%C3%B6dynnetty-testej%C3%A4}

Kloonaa projekti [https://github.com/nyluntu/saliavustaja](https://github.com/nyluntu/saliavustaja)

Käynnistä projekti Visual Studiolla. Yritä kääntää projekti, jotta kaikki riippuvuudet ladataan. Tämän jälkeen valitse projekteista Saliavustaja.UI. Projektin päällä klikkaa hiiren oikeata painiketta ja kontekstimenusta valitse "set as startup project". Tämän jälkeen käynnistä projekti ja kokeile, että ohjelma käynnistyy.

Seuraavaksi sulje ohjelma ja tutustu SaliavustajaTests -projektiin. Yritä saada ajettua testit Visual Studiolla. Yritä tehdä havaintoja testeistä:

* Mitä testit testaavat? Mitä ne siis yrittävät todistaa?
* Miten testiluokat on nimetty?
* Miten testimetodit on nimetty?
* Miten eri attribuutteja on käytetty?
* Miten eri Assert-tarkistuksia on käytetty?
* Miten itse testit on rakenteeltaan ja luettavuudeltaan kirjoitettu?

#### Arrange-Act-Assert -sääntö testien kirjoittamisessa {#arrange-act-assert--s%C3%A4%C3%A4nt%C3%B6-testien-kirjoittamisessa}

Tutustu seuraavaan artikkeliin. [http://wiki.c2.com/?ArrangeActAssert](http://wiki.c2.com/?ArrangeActAssert)

Mikä on Arrange, Act, Assert säännön tarkoitus=

Tutustu edelliseen Saliavustaja esimerkkiin ja huomioi, toteutuuko siellä kyseinen rakenne?

Mitä muita tapoja on järjestellä yksikkötestien ohjelmointikoodia?

#### Merkkijono laskin -ohjelman toteuttaminen yksikkötestein {#merkkijono-laskin--ohjelman-toteuttaminen-yksikk%C3%B6testein}

Seuraava harjoitus ei ole kirjoittajan oma vaan perustuu Roy Osheroven String Calculator harjoitukseen. [http://osherove.com/tdd-kata-1/](http://osherove.com/tdd-kata-1/)

Vältä katsomasta vastauksia vaan keskity seuraavan tehtävänannon ohjeistukseen ja yritä ratkaista se ensin itse niin pitkälle kuin pääset. Harjoituksen tavoitteena on luoda yksinkertainen ohjelma, joka on tarkoit määritelty ja sen oikea toiminnallisuus tulee todistaa testien avulla.

**Merkkijono laskin**

Tee laskin, joka ottaa numerot String -tyyppisenä vastaan. Ei siis double tai int tai muuna numeromuotona. Luo ohjelma alla mainittujen vaatimuksiin perustuen siten, että sinulla on vähintään yksi testi jokaiselle vaatimukselle. Kun olet kirjoittanut testin, voit vielä tehdä ohjelmasta konsoliohjelman.

Ohjelman tulee toimia siten, että luokan nimi, joka toteuttaa kyseisen vaatimuksen nimi on MerkkijonoLaskin. Luokalla on metodi Laske\(string laskutoimitus\), jolla on yksi string parametri. Kun laskutoimitus on laskettu, palauttaa metodi Int tyyppisen lukuarvon, joka vastaa laskutoimituksen tulosta.

* \[ \] Tyhjä merkkinojo palauttaa nollan.
* \[ \] Yksi numero, laskin palauttaa annetun numeron arvon..
* \[ \] Kaksi numeroa, pilkulla erotettuna, palauttaa lukujen summan.
* \[ \] Toteuta ominaisuus, että numeroita voidaan antaa pilkulla erotettuna rajoittamaton määrä ja laskin palauttaa lukujen summan.
* \[ \] Toteuta ominaisuus, että pilkkujen tilalla voidaan käyttää newline merkintää lukujen erottimena pilkkujen sijaan. \(newline = \n\)
  * Esimerkiksi arvo "1\n2,3" palauttaisi summan 6.
  * Ei tarvitse tukea muotoa, jossa erottimet seuraavat toisiaan. Esimerkiksi "1,\n". Voidaan olettaa, ettei tällaisia syötteitä anneta.
* \[ \] Negatiivinen luku, pienempi kuin nolla, aiheuttaa virheen. \(Exception\)
* \[ \] Luvut, jotka ovat yli 1000, ei huomioida yhteenlaskussa.

#### FizzBuzz -ohjelman toteuttaminen yksikkötestein {#fizzbuzz--ohjelman-toteuttaminen-yksikk%C3%B6testein}

Tutustutaan klassikoksi muodostuneeseen ohjelmointiongelmaan:

> Kirjoita ohjelma, joka kysyy käyttäjältä lukua yhden ja sadan väliltä ja tulostaa luvun. Jos luku on kolmella jaollinen, luvun sijaan tulostetaan "Fizz". Jos luku on viidellä jaollinen, luvun sijaan tulostetaan "Buzz". Jos luku on sekä kolmellä että viidellä jaollinen, luvun sijaan tulostetaan "FizzBuzz".

Ohjelma voi olla sinulle tuttu. Nyt tavoitteena on tehdä ohjelma ensin yksikkötestien kanssa ja vasta lopuksi toteuttaa konsoliohjelma syötteiden kysymiseen. Tarkoituksena on oppia erottamaan testikoodi niin sanotusta tuotantokoodista. Yritä, että saisit testien avulla varmistettua ensin ohjelman toimivuuden. Alla annettu vielä apuja ohjelman toteuttamiseen osissa;

1. Tee ohjelma, joka lukee luvun käyttäjältä ja tulostaa sen.
2. Jos luku on jaollinen kolmella, tulosta luvun sijaan merkkijono "Fizz".
3. Jos luku on jaollinen viidellä, tulosta luvun sijaan merkkijono "Buzz".
4. Jos luku on jaollinen kolmella ja viidellä, tulosta luvun sijan merkkijono "FizzBuzz".

_Ps. Tehtävänannossa puhutaan tarkoituksella, että käyttäjä antaa syötteen. Lopullisen ohjelman tulisi toimia tällä tavoin mutta sinun tehtäväsi on pohtia, miten esimerkiksi käyttäjän syöte tulee huomioitua testeissä. Tarvitseeko sitä edes testata? Perustele vastauksesi tai kerro oma toteutustapasi tälle._

#### Keilauksen pistelaskuri {#keilauksen-pistelaskuri}

Tutustu alla olevaan tehtävänantoon. Sinun tehtäväsi on toteuttaa ohjelma käyttäen yksikkötestausta. Tehtävänanto on tarkoituksella jätetty pilkkomatta pieniin välivaiheisiin. Sinun pitää itse lähteä purkamaan tehtävänantoa ja miettiä mitä testaisit ensin tai mistä lähtisit liikkeelle. Voit aloittaa vaikka hahmottelemalla miten ohjelma toimii.

Tee itsellesi muistiinpanot, miten tehtävän ratkaisisit. Kun sinulla on jonkinlainen ajatus niin yritä toteuttaa ratkaisusi. Alkuun voit esimerkiksi listata helpoimmat testit, jotka vievät ohjelman kokonaisuutta eteenpäin.

> Yksi keilasarja koostuu kymmenestä ruudusta. Yhdeksään ensimmäiseen ruutuun saa heittää kaksi heittoa, jos ensimmäinen heitto ei ole kaato ja kymmenenteen ruutuun heitetään kolme heittoa, jos ensimmäinen heitto on kaato tai toinen heitto on paikko.
>
> Jokaisesta heitosta saa pisteitä yhtä paljon kuin on kaadettuja keiloja. Jos heitto on kaato, kyseisen ruudun pisteisiin lasketaan mukaan lisäksi kahden seuraavan heiton pisteet ja paikon jälkeen lasketaan ruutuun mukaan seuraavan yhden heiton pisteet.
>
> Ruudun pisteet lasketaan ja merkitään vasta kun kaikki ruutuun tarvittavat heitot on heitetty, esimerkiksi kaadon jälkeen on heitettävä ensin kaksi heittoa ennen kuin pisteet voidaan laskea.
>
> Maksimipisteet 300 saadaan, kun heitetään 12 kaatoa peräkkäin, jolloin jokaista ruutua kohti tulee 30 pistettä.
>
> \(alkuperäinen idea \[[http://codingdojo.org/kata/Bowling/](http://codingdojo.org/kata/Bowling/)\]\([http://codingdojo.org/kata/Bowling/](http://codingdojo.org/kata/Bowling/)\)\)

