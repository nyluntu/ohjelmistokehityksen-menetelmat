---
description: 'Kuvattu tehtävä tunneille, josta lähdetään liikkeelle.'
---

# Projekti 2018/01 Perjantaille 14.9

## Ominaisuus

Verkkokaupasta tehdyn tilauksen vastaanottaminen

## Käyttäjätarina\(t\)

Alla on kopioitu alkuperäisestä toimeksiannosta käyttäjätarinat. Nämä on määritetty tässä kohdin tärkeimmiksi, jotta projektissa päästään alkuun ja voidaan kokeilla ensimmäistä versiota.

Käyttäjätarinoita oli valittujen lisäksi monia muita, jotka "rikastavat" ohjelman ominaisuuksia. Näitä ei kuitenkaan koettu vielä tärkeäksi vaan voidaan sinnitellä ilman niitä. 

Kokonaisuutena ominaisuus ei välttämättä ole valmis valittujen käyttäjätarinoiden jälkeen mutta ohjelman julkaisu on asiakkaan päätettävissä. Ensimmäisessä versiossa on tarkoitus kokeilla vain tilauksen tekeminen kokonaisuutena ja seuraavissa vaiheissa lisätä ominaisuuksia.

Käyttäjätarinoiden kulkua on tarkennettu alla käyttötapausten avulla.

| Tunniste | As a/an | I want to... | so that |
| :--- | :--- | :--- | :--- |
| Tarina 01 | Yritysasiakkaana | tahdon pystyä poimimaan tilaukseen haluamani tuotteita | voin luoda haluamani tilauksen. |
| Tarina 02 | Toimittajana | tahdon nähdä listan uusista käsittelemättömistä tilauksista | voin tietää mitkä tilaukset minun tulisi käsitellä ja lähettää. |

## Käyttötapauskuvaukset

### Tarina 01

Yritysasiakkaana \(jäljempänä asiakas\) tahdon pystyä poimimaan tilaukseen haluamani tuotteita, jotta voin luoda haluamani tilauksen

Alla kuvattu eri tapaukset käyttäjätarinaan liittyen.

{% tabs %}
{% tab title="TAPAUS 01" %}
#### TAPAUS 01

**Tavoite**

Verkkokauppaohjelmistoa käyttävä asiakas saa lisättyä vahvistamattomaan tilaukseena tuotteita.

**Esiehdot**

* Ohjelmassa on oltava saatavilla olevia tuotteita, joita asiakas voi valita.

**Onnistunut lopputulos**

Asiakas näkee tilauksessaan tuotteen, jonka hän on toiminnon aikana valinnut.

**Virheellinen lopputulos**

Asiakkaan valitsema tuote ei näytä tilauksessa. Ohjelma ei kaadu mikäli virhe sattuu vaan ilmoittaa virheellisestä toimenpiteestä.

**Kuvaus käyttötapauksesta**

1. Asiakas saa listan valittavista tuotteista.
2. Asiakas valitsee tuotteen listalta ja hyväksyy sen tilaukseen.
3. \(järjestelmä lisää tässä kohdin tuotteen tilaukseen\)
4. \(järjestelmä ilmoittaa asiakkaalle, että tuote on lisätty tilaukseen\)

**Kuvaus virheellisestä käyttötapauksesta**

**Kohdassa 3** tuotteen lisäys tilaukseen ei onnistu. **Kohdan 4** sijaan ohjelman tulisi ilmoittaa asiakkaalle, että tuotetta ei voitu lisätä tilaukseen.
{% endtab %}

{% tab title="TAPAUS 02" %}
#### TAPAUS 02

**Tavoite**

Verkkokauppaohjelmistoa käyttävä asiakas saa vahvistettua tilauksen.

**Esiehdot**

* Ohjelmassa on oltava saatavilla olevia tuotteita, joita asiakas voi valita.
* Asiakkaan on täytynyt lisätä tilaukseen vähintään yksi tuote.

**Onnistunut lopputulos**

Asiakas näkee ohjelmassa ilmoituksen onnistuneesta tilauksen luomisesta.

**Virheellinen lopputulos**

Järjestelmä ilmoittaa, ettei tilausta saada luotua. Tilaus ei jää talteen.

**Kuvaus käyttötapauksesta**

1. Asiakas valitsee vahvistettavan tilauksen.
2. Asiakas täyttää yhteystietonsa.
3. Asiakas näkee tilauksesta yhteenvedon.
   1. Katso välilehti \(**tilauksen yhteenveto**\)
4. Asiakas vahvistaa tilauksen.
5. \(järjestelmä käsittelee tilauksen\)
6. \(järjestelmä ilmoittaa asiakkaalle onnistuneen tilauksen luomisesta\)

**Kuvaus virheellisestä käyttötapauksesta**

**Kohdassa 5** tilauksen vahvistaminen ei onnistu jostakin seuraavista syistä ja ilmoittaa siitä asiakkaalle:

* Tilauksessa ei ole tuotteita.
* Asiakas ei ole antanut yhteystietoja, kaikki kentät pakollisia.
{% endtab %}

{% tab title="Tilauksen yhteenveto" %}
* Tuotteet erotettu tuoteriveihin.
* Tuotteiden määrät kerrottu tuoteriveittäin sekä yhteensä.
* Tuotteiden hinnat kerrottu tuoteriveittäin sekä tilauksen kokonaissumma.
* Hinnoista kerrottu kaksi eri hintaa, arvonlisäveron kanssa \(24%\) sekä ilman arvonlisäveroa \(0%\)
* Asiakkaan yhteystietoihin kuuluu:
  * Etunimi, Sukunimi, Toimitusosoite, y-tunnus, puhelinnumero, sähköposti.
{% endtab %}
{% endtabs %}

### Tarina 02

Toimittajana tahdon nähdä listan uusista käsittelemättömistä tilauksista, jotta voin tietää mitkä tilauksen minun tulisi käsitellä ja lähettää.

Alla kuvattu eri tapaukset käyttäjätarinaan liittyen.

{% tabs %}
{% tab title="TAPAUS 01" %}
**TAPAUS 01**

**Tavoite**

Saapuneiden tilauksien käsittelijänä minun tulisi pystyä näkemään lista uusista tilauksista.

**Esiehdot**

* Yritysasiakas on tehnyt vähintään yhden onnistuneen tilauksen järjestelmään.

**Onnistunut lopputulos**

Tilauksen käsittelijä näkee listan yritysasiakkaiden tekemistä vahvistetuista tilauksista.

**Virheellinen lopputulos**

Tilauksen käsittelijä ei näe vahvistettuja tilauksia.

**Kuvaus käyttötapauksesta**

1. Tilauksen käsittelijä valitsee "uudet tilaukset"
2. \(järjestelmä hakee vahvistetut tilaukset ja näyttää listan tilauksen käsittelijälle\)
   1. Katso välilehti \(**tilauksien listaus**\)

**Kuvaus virheellisestä käyttötapauksesta**

**Kohdassa 2** jos jostain syystä tilauksia ei saada luettua, tulisi ohjelman ilmoittaa siitä tilauksen käsittelijälle sopivalla viestillä.
{% endtab %}

{% tab title="TAPAUS 02" %}
**TAPAUS 02**

**Tavoite**

Saapuneiden tilauksien käsittelijänä minun tulisi pystyä yksittäisen tilauksen yhteenveto.

**Esiehdot**

* Yritysasiakas on tehnyt vähintään yhden onnistuneen tilauksen järjestelmään.

**Onnistunut lopputulos**

Tilauksen käsittelijä näkee saapuneesta tilauksesta yhteenvedon.

**Virheellinen lopputulos**

Tilauksen käsittelijä ei näe tilauksen yhteenvetoa.

**Kuvaus käyttötapauksesta**

1. Tilauksen käsittelijä valitsee saapuneen tilauksen.
2. Tilauksen käsittelijä näkee tilauksesta yhteenvedon.
   1. Katso välilehti edellisestä tarinasta \(**tilauksen yhteenveto**\)

**Kuvaus virheellisestä käyttötapauksesta**

**Kohdassa 2** jos jostain syystä tilausta ei saada luettua, tulisi järjestelmän ilmoittaa siitä viestillä tilauksen käsittelijälle.
{% endtab %}

{% tab title="Tilauksien listaus" %}
Saapuneiden tilauksien listassa tulisi näkyä seuraavat tiedot.

* Tilauspäivämäärä
* Asiakkaan nimi
* Asiakkaan puhelinnumero
* Tilauksessa olevien tuotteiden kokonaismäärä
* Tilauksen kokonaissumma. \(alv24 ja alv0\)
{% endtab %}
{% endtabs %}

## Tehtävän tavoitteita

{% hint style="warning" %}
Harjoituksessa on rajattu toteutusvaihtoehtoja seuraavasti:

* Käyttöliittymä sovellukselle on konsolipohjainen. 
* Ohjelmointikieli on C\#
* Työkaluna toteutukselle Visual Studio 2017, myös Mac versio käy. Valitse siis sieltä projektiksi Console Project.

Tehtävä tehdään ryhmissä. Ryhmien tulee tehdä tehtävän osia käyttäen versionhallintaa ja Gitlab palvelua. 

Tehtävät tulee listata Gitlab palveluun.

Tehtävää tehdään niin pitkälle kuin mahdollista. Ohjaaja auttaa tunnilla.

Tehtävä toimii projektin aloituksena, joten tehkää jo heti alkuun siten, että ryhmän jäsenet tulevat jatkamaan tämän työn parissa seuraavat viikot. Tehtävää ei tulla aloittamaan uudelleen. Myöhemmin projektin edetessä ryhmä päättää joistakin tulevista tehtävistä mutta tämä lähtökohta pysyy kaikilla samana.
{% endhint %}



