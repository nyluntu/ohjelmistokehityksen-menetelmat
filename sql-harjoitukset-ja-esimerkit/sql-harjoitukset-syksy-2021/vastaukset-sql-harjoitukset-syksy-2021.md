# Vastaukset SQL harjoitukset syksy 2021

## Yksinkertaiset haut

{% hint style="info" %}
Seuraavat hakukyselyt koostuvat yhden taulun tietojen käytöstä.
{% endhint %}

Hae tietokannasta sen elokuvan tiedot, jonka tunniste on 351.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-16.41.06.png)

Hae tietokannasta elokuvan tunniste, nimi, julkaisuvuosi, pituus ja luokitus, jonka tunniste on 633.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-16.43.36.png)

Tee edellinen haku uudelleen mutta nimeä uudelleen haettujen tulosten sarakkeiden nimet suomeksi englannin sijaan siten, että tuloksessa lukee **elokuvan tunniste, elokuvan nimi, julkaisuvuosi, pituus, luokitus**.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-16.51.11.png)

Hae elokuvat, joiden pituus on yli 60 minuuttia. Näytä vain ensimmäiset 10 tulosta.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-16.55.15.png)

Tee edellinen haku uudelleen mutta tarkenna hakuehtoa vielä siten, että etsit vain PG-13 luokituksen saaneita elokuvia.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-16.56.43.png)

Hae 15 elokuvaa järjestettynä niiden keston mukaan pisimmästä lyhyimpään.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-16.59.44.png)

Hae 10 elokuvaa järjestettynä keston mukaisesti pisimmästä lyhyimpään, jotka kuuluvat PG-13 tai R -luokitukseen.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.02.20.png)

Tee edellinen haku uudestaan mutta aseta hakuehdoiksi luokitukset G ja NC-17. Toteuta hakuehto käyttäen **IN** operaattoria.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.03.22.png)

Hae lista kaikista elokuvista, joiden kesto on välillä 40 - 80 minuuttia. Järjestä pituuden mukaan pisimmästä lyhyimpään. \(yhteensä tuloksia tulisi olla 253 kpl\)

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.07.50.png)

Tee edellinen haku uudelleen mutta aseta hakuehdoksi 30-60 minuuttia. Toteuta hakuehto käyttäen **BETWEEN** operaattoria. \(yhteensä tuloksia tulisi olla 104 kpl\)

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.10.14.png)

Mikä on kaikkien elokuvien keskimääräinen kesto? Entä lyhimmän elokuvan kesto? Entä pisimmän elokuvan kesto?

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.12.55.png)

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.16.53.png)

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.17.14.png)

Hae uudelleen elokuvien keskimääräinen kesto mutta pyöristä luku kokonaisluvuksi.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.18.56.png)

Ryhmittele elokuvat luokituksen mukaan, jotta saat selville elokuvien määrän eri luokituksissa.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.41.11.png)

Tee edellinen haku uudelleen mutta näytä tulokset pienimmästä suurimpaan.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.43.02.png)

Etsi niiden asiakkaiden tiedot, joiden etunimi alkaa **"carol"**.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.50.27.png)

Tee edellinen haku uudelleen mutta yhdistä tuloksessa asiakkaan etunimi ja sukunimi yhdeksi sarakkeeksi **"nimi"**.

> _Mallikuvassa nimi -sarake on nimetty väärin sukunimi -sarakkeeksi._

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.52.28.png)

Etsi niiden asiakkaiden tiedot, joiden sähköpostissa esiintyy merkit **"martin"**.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.54.08.png)

Etsi niiden elokuvien määrä, joiden kuvauksessa esiintyy sana **"amazing"**.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-17.57.10.png)

## Haastavammat haut

{% hint style="info" %}
Seuraavissa hakukyselyissä tarvitaan edellisten kohtien oppeja. Tulosten hakemiseen tarvitaan myös JOIN -operaattorin käyttöä.
{% endhint %}

Selvitä asiakkaan, jonka tunniste on 85, kokonimi, sähköposti ja hänen osoitetiedoissaan oleva kadunnimi. 

![](../../.gitbook/assets/screen-shot-2021-09-08-at-18.02.47.png)

Tee edellinen haku uudelleen mutta lisää vielä tulokseen mukaan asiakkaan postinumero, kaupunki ja maa.

![](../../.gitbook/assets/screen-shot-2021-09-08-at-18.06.41.png)

Muuta edellisen haun ehtoja. Tarkenna hakua ja etsi kaikki ne asiakkaat, joiden maa on Saksa \(germany\). 

![](../../.gitbook/assets/screen-shot-2021-09-08-at-18.09.02.png)

