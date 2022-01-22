---
description: Harjoitustietokanta https://dev.mysql.com/doc/sakila/en/
---

# Mysql perusteet 106

Kirjoita SQL kyselyt, jotka vastaavat alla oleviin kysymyksiin. Yhteen kysymykseen voi liittyä yksi tai useampia SQL lauseita, joten ratkaisutavalla ei sinällään ole väliä kunhan siinä on käytetty SQL -kyselyitä.

Vältä vastausten katsomista etukäteen mutta ne auttavat, jos muuten jää jossakin kohdin jumiin.

Jos vastausta ei silti löydy, niin yritä silloin selittää itsellesi vastauksen SQL kysely ja selvittää mitä se varsinaisesti teki. Esimerkiksi vieraat SQL komennot.

#### 1. DVD -formaattien vuokraus on laskemaan päin. Myymälöihin on tarkoitus alkaa ostaa myös Blu-ray sekä 3D Blu-ray elokuvia. Kirjoita komennot mitä tarvitset luodaksesi taulun jakeluformaateille kun sen sisältö ja rakenne on alla kuvatun mukainen.

Taulun nimeksi tulee **format\_type** ja sen sarakkeet ovat:

* **type\_id**, pääavain, nouseva kokonaisluku, ei voi olla tyhjä, täytyy olla uniikki.
* **name**, merkkijono, sisältää jakelutyypin, esimerkiksi DVD, Blu-ray, 3D Blu-ray jne.
* **information\_url**, merkkijono, sisältää linkin jakeluformaatin lisätietoihin, esimerkiksi [https://fi.wikipedia.org/wiki/Blu-ray](https://fi.wikipedia.org/wiki/Blu-ray)

**2. Muuta taulun film -rakennetta siten, että lisäät siihen alla olevan kuvan mukaisen kentän. Kirjoita tarvittavat komennot. Selitä myös minkä tyyppinen viittaus (relaatio) tässä on kyseessä. (lue myös** [**ER -kaaviosta**](../../relaatiotietokannat/er-kaaviot.md)**)**

* uusi kenttä on nimeltään **type\_id**.
* kentän pitää toimia viiteavaimena edellisessä vaiheessa luomaasi "format\_type" tauluun.
* oletusarvon pitää viitata DVD -jakeluformaattiin.
* kun teet muutoksen niin kaikkien aiempien elokuvien formaatiksi voit asettaa DVD.
* Muuta yhden elokuvan formaatiksi Blu-ray ja toisen elokuvan formaatiksi 3D Blu-ray.

**3. Kehittäjänä huomaat ongelman, että elokuville voi asettaa vain yhden jakeluformaatin. yhdellä elokuvalla voi kuitenkin olla useita eri jakeluformaatteja, joten tarvitsemme liitostaulun. Kirjoita tarvittavat komennot taulun luomista varten. Selitä myös minkä tyyppinen viittaus (relaatio) tässä on kyseessä. (lue myös** [**ER -kaaviosta**](../../relaatiotietokannat/er-kaaviot.md)**)**

Taulun nimeksi tulee **film\_types** ja sen sarakkeet ovat:

* **film\_id**, tauluun film viittaava arvo, yksi osa pääavainta.
* **type\_id**, tauluun format\_type viittaava arvo, toinen osa pääavainta.
* Huomaa, että edelliset sarakkeet yhdessä ovat taulun pääavain.

**4. Liitostaulun myötä edellä luotua **_**film**_** taulun **_**type\_id**_** -saraketta ei enää tarvita. Kirjoita komennot, jolla voit poistaa kyseisen sarakkeen ja sitä ennen päivittää uuteen **_**film\_types**_** -tarvittavat tiedot.**

**5. Millä komennoilla saat kumottua edellisissä vaiheissa tehdyt muutokset? Kirjoita siis komennot, joilla voit poistaa **_**format\_type**_** ja **_**film\_types**_** taulut kaikkine tietoineen.**
