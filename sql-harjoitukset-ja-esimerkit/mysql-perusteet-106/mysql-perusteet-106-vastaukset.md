# mysql-perusteet-106-vastaukset

#### 1. DVD -formaattien vuokraus on laskemaan päin. Myymälöihin on tarkoitus alkaa ostaa myös Blu-ray sekä 3D Blu-ray elokuvia. Kirjoita komennot mitä tarvitset luodaksesi taulun jakeluformaateille kun sen sisältö ja rakenne on alla kuvatun mukainen.

Taulun nimeksi tulee **format\_type** ja sen sarakkeet ovat:

* **type\_id**, pääavain, nouseva kokonaisluku, ei voi olla tyhjä, täytyy olla uniikki.
* **name**, merkkijono, sisältää jakelutyypin, esimerkiksi DVD, Blu-ray, 3D Blu-ray jne.
* **information\_url**, merkkijono, sisältää linkin jakeluformaatin lisätietoihin, esimerkiksi [https://fi.wikipedia.org/wiki/Blu-ray](https://fi.wikipedia.org/wiki/Blu-ray)

```sql
-- Luodaan tehtävänannon mukainen taulu.
CREATE TABLE format_type(
    type_id SMALLINT NOT NULL AUTO_INCREMENT PRIMARY KEY,
    NAME VARCHAR(32),
    information_url VARCHAR(100)
)

-- Asetetaan luotuun tauluun malliksi kolme erilaista levyformaattia.
INSERT INTO format_type(type_id, name, information_url)
VALUES 
( NULL, 'DVD', 'https://fi.wikipedia.org/wiki/DVD' ),
( NULL, 'Blu-ray', 'https://fi.wikipedia.org/wiki/Blu-ray' ),
(  NULL, '3D Blu-ray', 'https://en.wikipedia.org/wiki/List_of_Blu-ray_3D_releases' );
```

**2. Muuta taulun film -rakennetta siten, että lisäät siihen alla olevan kuvan mukaisen kentän. Kirjoita tarvittavat komennot. Selitä myös minkä tyyppinen viittaus \(relaatio\) tässä on kyseessä. \(lue myös** [**ER -kaaviosta**](../../relaatiotietokannat/er-kaaviot.md)**\)**

* uusi kenttä on nimeltään **type\_id**.
* kentän pitää toimia viiteavaimena edellisessä vaiheessa luomaasi "format\_type" tauluun.
* oletusarvon pitää viitata DVD -jakeluformaattiin.
* kun teet muutoksen niin kaikkien aiempien elokuvien formaatiksi voit asettaa DVD.
* Muuta yhden elokuvan formaatiksi Blu-ray ja toisen elokuvan formaatiksi 3D Blu-ray.

```sql
-- Lisätään uusi sarake vanhaan olemassaolevaan film-tauluun
-- ja oletusarvoksi määritetään 1.
ALTER TABLE film ADD type_id SMALLINT DEFAULT 1

-- Sarakkeen luomisen jälkeen luodaan viiteavain edellisen tehtävän
-- format_type ja film -taulun välille. Käytetään siinä type_id-saraketta.
ALTER TABLE film
ADD CONSTRAINT FK_type_id
FOREIGN KEY(type_id) REFERENCES format_type(type_id)

-- Malliksi päivitetään kahdelle eri elokuvan nimikkeelle tämä eri formaatit.
-- type_id viitaa tässä format_type-taulun pääavaimeen.
UPDATE film SET type_id = 2 WHERE film_id = 1003
UPDATE film SET type_id = 3 WHERE film_id = 1
```

**3. Kehittäjänä huomaat ongelman, että elokuville voi asettaa vain yhden jakeluformaatin. yhdellä elokuvalla voi kuitenkin olla useita eri jakeluformaatteja, joten tarvitsemme liitostaulun. Kirjoita tarvittavat komennot taulun luomista varten. Selitä myös minkä tyyppinen viittaus \(relaatio\) tässä on kyseessä. \(lue myös** [**ER -kaaviosta**](../../relaatiotietokannat/er-kaaviot.md)**\)**

Taulun nimeksi tulee **film\_types** ja sen sarakkeet ovat:

* **film\_id**, tauluun film viittaava arvo, yksi osa pääavainta.
* **type\_id**, tauluun format\_type viittaava arvo, toinen osa pääavainta.
* Huomaa, että edelliset sarakkeet yhdessä ovat taulun pääavain.

```sql
-- Luodaan uusi film_types taulu ja samalla sille viiteavaimet
-- film ja format_type -taulujen kanssa.
CREATE TABLE film_types ( film_id SMALLINT UNSIGNED, type_id SMALLINT, PRIMARY KEY(film_id, type_id), 
CONSTRAINT FK_film_id FOREIGN KEY (film_id) REFERENCES film(film_id) on UPDATE CASCADE, 
CONSTRAINT FK_type1_id FOREIGN KEY (type_id) REFERENCES format_type(type_id) on UPDATE CASCADE);

```

**4. Liitostaulun myötä edellä luotua** _**film**_ **taulun** _**type\_id**_ **-saraketta ei enää tarvita. Kirjoita komennot, jolla voit poistaa kyseisen sarakkeen ja sitä ennen päivittää uuteen** _**film\_types**_ **-tarvittavat tiedot.**

```sql
-- Film-taulusta poistetaan ensin viitevain, joka on luotu edellisissä vaiheissa.
ALTER TABLE film DROP FOREIGN KEY FK_type_id;

-- Kun viiteavain on poistettu, voidaan poistaa type_id -sarake.
ALTER TABLE film DROP type_id;

-- Voidaan asettaa edellisen kohdan uudelle taululle myös oletusarvo
-- levyformaatiksi. Tämä ei ole pakollinen mutta toisaalta helpottaa 
-- asioita.
ALTER TABLE film_types  ALTER type_id SET DEFAULT 1;

-- Lisätään kaksi eri elokuvaa uuteen tauluun. Näille tulee oletuksena
-- DVD formaatti type_id -sarakkeen arvoksi.
INSERT INTO film_types (film_id) VALUES (3),(4);

-- Tässä yhdelle elokuvan nimikkeelle on määritetty kaksi eri levyformaattia.
-- Eli Blu-ray ja 3D Blu-ray. Film_id on tässä arvoltaan 5.
INSERT INTO film_types (film_id, type_id) VALUES (5,3),(5,2);
```

**5. Millä komennoilla saat kumottua edellisissä vaiheissa tehdyt muutokset? Kirjoita siis komennot, joilla voit poistaa** _**format\_type**_ **ja** _**film\_types**_ **taulut kaikkine tietoineen.**

```sql
-- Poistetaan film_types taulu.
DROP TABLE film_types;

-- Poistetaan format_type taulu.
DROP TABLE format_type;
```

