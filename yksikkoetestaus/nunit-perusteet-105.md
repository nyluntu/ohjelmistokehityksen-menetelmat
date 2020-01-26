# NUnit perusteet 105

## Merkkijono laskin -ohjelman toteuttaminen yksikkötestein

Seuraava harjoitus ei ole kirjoittajan oma vaan perustuu Roy Osheroven String Calculator harjoitukseen. [http://osherove.com/tdd-kata-1/](http://osherove.com/tdd-kata-1/)

Harjoitusta on hieman muutettu alkuperäisestä.

Vältä katsomasta esimerkkejä vaan keskity seuraavan tehtävänannon ohjeistukseen ja yritä ratkaista se ensin itse niin pitkälle kuin pääset. Harjoituksen tavoitteena on luoda yksinkertainen ohjelma, joka on tarkoin määritelty ja sen oikea toiminnallisuus tulee todistaa testien avulla.

## **Tavoite**

Oppia hyödyntämään yksikkötestausta sekä testivetoista kehitystä.

Pyri kirjoittamaan seuraava testi aina valmiiksi ja sitten vasta sitä vastaava tuotantokoodi.

### **Laskimen määritys**

{% hint style="info" %}
Tee yksi kohta kerrallaan. Vältä etenemästä seuraavaan ennen ratkaisua ja katsomatta liikaa muita vaatimuksia.

Kokeile myös ensin katsomatta esimerkkejä syötteistä mutta voit käyttää niitä sitten myös apuna.
{% endhint %}

Ohjelmassa on **MerkkijonoLaskin** niminen luokka. Luokassa on yksi metodi nimeltään **Laske.** Metodi palauttaa numeroarvon. **Laske** -metodi ottaa parametrikseen merkkijonon \(string\).

Luo ohjelma alla mainittujen vaatimuksiin perustuen siten, että sinulla on vähintään yksi testi jokaiselle vaatimukselle. Kun olet kirjoittanut testin, voit vielä tehdä ohjelmasta konsoliohjelman.

* \[ \] Tyhjä merkkinojo palauttaa nollan.
* \[ \] Yksi numero, laskin palauttaa annetun numeron arvon..
* \[ \] Kaksi numeroa, pilkulla erotettuna, palauttaa lukujen summan.
* \[ \] Toteuta ominaisuus, että numeroita voidaan antaa pilkulla erotettuna rajoittamaton määrä ja laskin palauttaa lukujen summan.
* \[ \] Toteuta ominaisuus, että pilkkujen tilalla voidaan käyttää newline merkintää lukujen erottimena pilkkujen sijaan. \(newline = \n\)
  * Esimerkiksi arvo "1\n2,3" palauttaisi summan 6.
  * Ei tarvitse tukea muotoa, jossa erottimet seuraavat toisiaan. Esimerkiksi "1,\n". Voidaan olettaa, ettei tällaisia syötteitä anneta.
* \[ \] Negatiivinen luku, pienempi kuin nolla, aiheuttaa virheen. \(Exception\)
* \[ \] Luvut, jotka ovat yli 1000, ei huomioida yhteenlaskussa.

### Esimerkkejä syötteistä

| Laske metodin parametri | Metodin palauttama arvo |
| :--- | :--- |
| "" | 0 |
| "0" | 0 |
| "1" | 1 |
| "2" | 2 |
| "1,1" | 2 |
| "3,4" | 7 |
| "2,7,4" | 13 |
| "5,5,5,4" | 19 |
| "1\n2,3" | 6 |
| "-1" | throw exception\("negatiivisia lukuja ei sallita\) |
| "3,-1" | throw exception\("negatiivisia lukuja ei sallita\) |
| "3,1001" | 3 |

