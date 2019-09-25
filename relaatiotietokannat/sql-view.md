---
description: >-
  View on niin sanotusti virtuaalinen taulu, joka muodostetaan halutusta
  kyselystä.
---

# SQL View

Tutustu aiheeseen lisää osoitteessa [http://www.mysqltutorial.org/mysql-views-tutorial.aspx](http://www.mysqltutorial.org/mysql-views-tutorial.aspx)

## Hyötyjä

### 1. Monimutkaisten hakujen "tallentaminen"

Relaatiotietokannoissa taulujen tietoja yhdistetään JOIN komennoilla. Kun tauluja on useampia, voi kyselystä tulla monimutkainen. Tällainen kysely voidaan tallentaa omaksi **"näkymäkseen"**, jolloin seuraavan kerran voidaan haku tehdä luotuun näkymään. Näkymä on siis virtuaalinen taulu, johon `SELECT` haku voidaan osoittaa.

### 2. Logiikan yhtenäistäminen

Voidaan ajatella tilanne, jossa luot esimerkiksi raportin tietokannan tiedoista. Raportti sisältäisi joitakin laskukaavoja mitkä on vaikea muistaa tai kirjoittaa hakuihin. Tähän tarpeeseen voidaan myös luoda näkymä, joka sisältää tällaiset laskukaavat, jotta jatkossa samojen tietojen hakeminen on yksinkertaisempaa.

Suppose you have to repeatedly write the same formula in every query.  Or you have a query that has complex business logic. To make this logic consistent across queries, you can use a view to store the calculation and hide the complexity.

### 3. Tietoturvan lisääminen

Kaikkea tietoa ei aina tule näyttää tietokannan käyttäjille. Tällaista arkaluonteista tietoa voidaan suodattaa pois hakukyselyllä ja muodostaa näkymä, joka ei sisällä arkaluonteista tietoa. Tietokannoissa voidaan sitten antaa näkymään oikeudet vain tietyille käyttäjille eikä heitä päästetä tekemään hakuja kaikista tauluista.

### 4. Yhteensopivuus vanhojen ohjelmien kanssa

Tietokannat muuttuvat ohjelman päivitysten yhteydessä. Usein tulee uusia tauluja tai vanhoista halutaan päästä eroon. Näkymät toimivat myös tällaisessa tilanteessa, että voidaan luoda esimerkiksi väliaikainen näkymä, joka muistuttaa vanhan version taulua. Tässä tilanteessa ohjelma saattaisi toimia normaalisti erilaisten päivitystöiden jälkeen, koska ohjelmalle ei ole väliä minkälaisesta taulusta tieto on haettu.

## Lähteet

{% embed url="http://www.mysqltutorial.org/mysql-views-tutorial.aspx" %}

