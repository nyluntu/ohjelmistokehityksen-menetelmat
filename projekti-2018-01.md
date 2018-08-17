---
description: >-
  Lukuun on luotu alustava kuvaus toteutettavasta ohjelmasta. Toimeksianto on
  harjoitusprojekti, johon sisältyy ajankohtaisista asiakasprojekteista
  poimittuja tilanteita.
---

# Projekti 2018/01

{% hint style="warning" %}
**Projektin toimeksianto on seuraava**

Kehitystiimin tulee lukea projektin kuvaus ja asiakkaan tarpeet läpi. Projektia on aloitettu jo työstämään yhdessä, jotta sen konteksti olisi tutumpi. Kun kehitystiimi aloittaa ohjelman jatkokehittämisen itsenäisesti, tulee heidän omatoimisesti näyttää, että osaavat soveltaa opetettuja ohjelmistokehitykseen liittyviä menetelmiä ja käytänteitä.

Kehitystiimi itse päättää projektin suunnan ja heillä on sitä varten olemassa ohjaaja, joka arvioi lopputuloksen. Projektissa pitää esiintyä kehitystiimin oma syventyminen ongelmaan, joten ennalta määritettyä lopputulosta ei ole. Omalla aktiivisuudellaan ja työskentelyllään kehitystiimi näyttää osaavansa asiat.

Ohjaaja arvioi projektin aikana syntyneitä dokumentteja mihin sisältyy mm. tehtävälista, käyttäjätarinat, käyttötapauskuvaukset, ohjelmakoodi, ohjelman valmis versio. Tämän lisäksi arvioihin voi olla muita vaikuttavia tekijöitä mutta nämä asiat on kerrottu selkeästi kehitystiimille.

_**Huom! Opiskelijoille suunnatuissa projekteissa heidän arviointinsa ja palautettavat dokumentit on kuvattu tarkemmin heidän omalla oppimisalustallaan.**_
{% endhint %}



## Tuotteen nimi / Projektin nimi

Verkkokaupan tilauksen vastaanottaminen ja käsittely

## Asiakkaan kuvaus tarpeista

Asiakkaalla on autojen varaosien myyntiin keskittynyt liiketoiminta. Nykyinen liiketoiminta tapahtuu pääsääntöisesti myymälöiden kautta yksityisasiakkaille. Liiketoiminnan kasvattamiseksi asiakas on päättänyt kasvattaa yrityksille ja muille yhteistyökumppaneille suunnattua myyntiä.

Yrityksille suunnattuja palveluita on olemassa mutta tilaukset on otettu vastaan puhelimitse tai sähköpostitse. Tilauksien määrän kasvattamiseksi asiakas tarvitsee pienen ohjelmiston, joka vastaanottaa tilauksia ja käsittelee yleisimmät tilaukseen liittyvät vaiheet.

Asiakas on ajatellut työkalun olevan eräänlainen verkkokauppa, joka on suunnattu vain yritysasiakkaille. Tilausta tehdessä pitäisi olla mahdollista kertoa ostajan yhteystiedot tai muulla tapaa tunnistaa kuka tilauksen on tehnyt. Yritysasiakkaille on mahdollista olla tehty erilaisia sopimuksia, jotka määrittävät ostoksen kokonaissumman.

Tilaukseen tulisi pystyä valitsemaan ennalta määritettyjä tuotteita ja tilauksen vahvistamisen jälkeen, asiakkaalla pitää olla tapa nähdä uudet tulleet tilaukset sekä pystyä merkitsemään ne lähetetyksi ostajalle.

Koska kyse on autojen varaosista, ei asiakkaalla aina ole kyseisiä tuotteita varastossa ja hän joutuu tehdä siitä erillisen toimitus/tilauspyynnön maahantuojille. Tällöin tilausta tehdessä ostajalle pitäisi ilmoittaa, että varaosien toimituksessa voi kestää normaalia pidempään.

## Tuotteen tehtävälista

Tuotteen tehtävälista koostuu pääosin alla mainituista kokonaisuuksista, joita on tarkennettu myöhemmin käyttäjätarinoiden ja käyttötapausten avulla.

* Tuotteiden lisääminen ja hallinta
* Tilauksen luominen, hyväksyntä ja hallinta
* Asiakkaan lisääminen ja hallinta
* Asiakkaan erikoishintojen lisääminen ja hallinta
* Varaston hallinta tilausten perusteella

### Käyttäjätarinat

Eri rooleille tai käyttäjäryhmille on tehty oma listauksensa heille tarkoitetuista ominaisuuksista. Listaukset eivät ole täydellisiä tai niihin ei ole otettu mukaan kaikkia ominaisuuksia. Tarkoituksena on pitää listat esimerkkien vuoksi yksinkertaisina.

#### Yritysasiakkaan käyttäjätarinat

| As a/an | I want to... | so that |
| :--- | :--- | :--- |
| Yritysasiakkaana | tahdon pystyä poimimaan tilaukseen haluamani tuotteita | voin luoda haluamani tilauksen. |
| Yritysasiakkaana | tahdon pystyä poistamaan tilauksestani tuotteita ennen sen vahvistamista | voin välttyä tilaamasta varaosia, joita en tarvitse. |
| Yritysasiakkaana | tahdon nähdä tilauksen yhteenvedon yhteydessä maininnan toimitusajasta tuotteiden osalta joita ei ole heti saatavilla | voin tietää tulevatko kaikki tuotteet samassa lähetyksessä. |
| Yritysasiakkaana | tahdon saada tilauksesta tilausvahvistuksen |  |
| Yritysasiakkaana | tahdon saada tilauksesta lähetysvahvistuksen | voin tietää milloin toimitus on lähetetty toimittajalta. |
| Yritysasiakkaana | tahdon nähdä tilauksen kokonaissumman ennen sen vahvistamista |  |

#### Verkkokaupan ylläpitäjän \(toimittaja eli tässä varsinainen projektin asiakas\) käyttäjätarinat

| As a | I want to... | so that |
| :--- | :--- | :--- |
| Toimittajana | tahdon nähdä listan uusista käsittelemättömistä tilauksista | voin tietää mitkä tilaukset minun tulisi käsitellä ja lähettää. |
| Toimittajana | tahdon saada tilauksesta keräilylistan | voin pakata yhden tilauksen tuotteet. |
| Toimittajana | tahdon pystyä vaihtamaan tilattujen tuotteiden yksikkömääriä | voin korjata inventaarivirheistä johtuvat virhetilanteet. |
| Toimittajana | tahdon nähdä listan kaikista tehdyistä tilauksista | voin tarkistaa tilauksien tiedot myöhemmin sen lähettämisen jälkeen. |
| Toimittajana | tahdon pystyä muodostamaan ja lähettämään laskun asiakkaalle tilauksen lähettämisen jälkeen | asiakkailtani perittävät myyntisaamiset tulevat hoidettua nopeammin. |
| Toimittajana | tahdon saada yhteenvedon varastosta loppuneista tuotteista | osaan tilata tuotteita lisää varastooni jo valmiiksi. |

### Käyttötapaukset

Käyttötapauksien kohdalla yksi käyttäjätarina pilkotaan tarkemmin vaiheisiin ja tapahtumiin mistä se koostuu. Käyttötapauksia ei ole kirjoitettu kaikista käyttätarinoista valmiiksi vaan niitä luodaan sen mukaan kuinka projekti etenee.

