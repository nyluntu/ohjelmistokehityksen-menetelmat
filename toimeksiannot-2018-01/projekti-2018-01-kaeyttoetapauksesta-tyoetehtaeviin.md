---
description: >-
  Esitelty tapa tai enemmän se oma tapa lähteä purkamaan toimeksiantoa
  pienempiin konkreettisimpiin tehtäväkokonaisuuksiin.
---

# Projekti 2018/01 Käyttötapauksesta työtehtäviin

## Valittu käyttäjätarina

**KOPIO** edellisistä esimerkeistä.

Yritysasiakkaana ** **_**(jäljempänä asiakas)**_** ** tahdon pystyä _**poimimaan tilaukseen**_ haluamani _**tuotteita,**_ jotta voin luoda haluamani tilauksen.

## Tarinan ensimmäinen käyttötapaus

**KOPIO** edellisistä esimerkeistä.

{% tabs %}
{% tab title="TAPAUS 01" %}
#### TAPAUS 01

**Tavoite**

Verkkokauppaohjelmistoa käyttävä _**asiakas**_ saa lisättyä _**vahvistamattomaan tilaukseen**_ tuotteita.

**Esiehdot**

* Ohjelmassa on oltava _**saatavilla olevia tuotteita**_, joita asiakas voi valita.

**Onnistunut lopputulos**

Asiakas näkee tilauksessaan tuotteen, jonka hän on toiminnon aikana valinnut.

**Virheellinen lopputulos**

Asiakkaan valitsema tuote ei näytä tilauksessa. Ohjelma ei kaadu mikäli virhe sattuu vaan ilmoittaa virheellisestä toimenpiteestä.

**Kuvaus käyttötapauksesta**

1. Asiakas saa listan valittavista tuotteista.
2. Asiakas valitsee tuotteen listalta ja hyväksyy sen tilaukseen.
3. (järjestelmä lisää tässä kohdin tuotteen tilaukseen)
4. (järjestelmä ilmoittaa asiakkaalle, että tuote on lisätty tilaukseen)

**Kuvaus virheellisestä käyttötapauksesta**

**Kohdassa 3** tuotteen lisäys tilaukseen ei onnistu. **Kohdan 4** sijaan ohjelman _**tulisi ilmoittaa asiakkaalle, että tuotetta ei voitu lisätä tilaukseen**_.
{% endtab %}
{% endtabs %}

## VAIHE 1: Käyttöliittymän luonnokset

Kun asia on vieras ja siitä on saatu kyseltyä kaikki mahdollinen, hyvä tapa lähteä liikkeelle on tehdä käyttöliittymä luonnoksia. Vastataan siis kysymykseen:&#x20;

_Miltä ohjelma tulisi näyttämään ja sen käyttö tuntumaan?_

{% hint style="info" %}
Helpoin tapa on paperi ja kynä, sitten erilaiset luonnosteluohjelmat jne. Mikä vain tuntuu luontevimmalta on aina hyvä lähtökohta. Alla esimerkki tähän harjoitukseen liittyen. Kuvat on tehty yksinkertaisesti tekstieditorilla ja otettu kuvakaappaukset.
{% endhint %}

### Kuvakaappaukset

![Ohjelman ensimmäinen näkymä tässä kohtaa sen historiaa.](../.gitbook/assets/screen-shot-2018-09-23-at-10.27.54.png)

![Ohjelman listaus tuotteista kun niitä on vain muutama kappale.](../.gitbook/assets/screen-shot-2018-09-23-at-10.28.04.png)

## VAIHE 2: Ohjelman rakenteen luokkakaavio

{% file src="../.gitbook/assets/20180921_riihimaki_ohjelmointiprojekti.html" %}
Ohjelman rakenteen luonnos
{% endfile %}

Liitteesstä _**"Ohjelman rakenteen luonnos"**_ on käyty läpi ohjelman rakennetta mitä se voisi olla teknisesti toteutettuna. Kyseessä on vain esimerkki omasta näkemyksestä ja se saa ja voi erota riippuen ohjelmoijasta.

Kaavioon on tuotu mukana olio-ohjelmoinnin piirteitä ja siksi siinä puhutaan luokista ja komponenteista. Kaavion tarkoitus ei ole kertoa miten ohjelmoida vaan taas tuoda erilainen näkökulma asiaan ja löytää lisää kysymyksiä mihin löytää vastaus... eli asioihin joita ei tiedetä.



## VAIHE 3: Analyysin jälkeen listatut työkokonaisuudet

Kun ohjelman rakennnetta ja vaatimuksia on käyty läpi, pitää vielä listata tehtäviä mistä lähdetään liikkeelle. Tässä tehtävät ovat vain listaus niistä asioista, josta ei tiedetä mitään ja ne pitää selvittää ennenkuin kokonaisuus saadaan tehtyä loppuun.

Seuraava kokonaisuus on taas hieman helpompi kun asia on tutumpi ja alun ongelmat ratkaistu.

### Käyttöliittymä

* Miten esitän tietoa käyttöliittymässä?
* Miten käyttöliittymän logiikka tai valintarakenne tulee toimimaan?
* Miten käyttöliittymän valintarakenne päivitetään?
* Miten otan käyttäjän antaman syötteen vastaan käyttöliittymästä?
* Miten määritän ohjelman tekemän toiminnon annetun syötteen perusteella?

### Ohjelman toiminnot

* Käytetäänkö luokkarakenteita vai ei?
* Mitä tietoja tai metodeita Tilaus-luokassa tulisi olla?
* Miten tilauksen luominen toimii kokonaisuudessaan?
* Miten tuotelistaus tulisi toimimaan?
* Onko tuotteet "kovakoodattu" vai luetaanko tiedostosta? (mitkä ovat näiden hyödyt ja haitat?)

### Tiedostojärjestelmä

* Miten tallennan yhden olion/luokan esimerkiksi tiedostoon?
* Käytetäänkö tekstitiedostoja, tietokantaa tai mitä tallennusratkaisua?
* Miten tallennan monimutkaisen olin/luokan esimerkiksi tiedostoon?
* Miten ohjelma lukee tallennetut tiedot kun se niitä tarvitsee?
* Missä tilanteissa ohjelma tallentaa tiedot?

## VAIHE 4: Ohjelmointi

Tässä kohdin on vain aloitettava ohjelmointi. Vasta sitten tiedetään oikeat ongelmakohdat ja puutteet tiedoissa. Sillä ei ole väliä miten tämä tulee tapahtumaan vaan yksi kerrallaan pyritään tekemään työkokonaisuus ja oppia sen kautta.

{% hint style="info" %}
Kun ohjelmoidaan, se ei tarkoita, että kaikki asiat pitää tietää ja osata. Sellaista tilannetta ei olekaan. On paljon tärkeämpää tunnistaa osa-alueet, joista ei tiedä mitään ja mitkä ovat haastavia, koska silloin niitä on tarkoitus osa-alueita on tarkoitus parantaa.
{% endhint %}

## Videot

Soittolista tähän liittyvistä asioista. Esittelee omia ajatuksia miten näihin työtehtäviin on päästy.

{% embed url="https://www.youtube.com/playlist?list=PL3iay_FdAzV_7GzGYkoO1msZPSLl1vIaz" %}
