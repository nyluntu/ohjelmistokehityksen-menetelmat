# Tehtävä 001 Tietokannan suunnittelu

## **Tehtävän tavoite**

Tietokannat ovat usein osa tietojärjestelmää ja ratkaisevat jonkin ongelman. Usein ongelmaan liittyy liiketoiminta minkä tueksi ratkaisua tehdään. Tehtävän tavoitteena on oppia tietokannan suunnittelun perusteita toimeksiannon ratkaisemiseksi.  


## Asiakkaan tarve

Riihimäen Lukutoukat Ry **\(jäljempänä Lukutoukat\)** on perustamassa pientä kirjalainaamoa jäsenilleen. Tässä he tarvitsevat apuasi sopivan järjestelmän tietokannan mallintamiseen.  
  
Lukutoukat ovat ajatelleet tarvitsevan pienen lainausjärjestelmän. Tietojärjestelmälle haetaan tukirahoja mutta sitä varten heillä tulisi olla tieto millainen palvelu tulee olemaan. 

Lukutoukat ovat kuulleet, että tietokanta on tässä isossa osassa ja pyytävät sinulta apua suunnittelemaan heidän tarpeisiinsa sopivan tietokantaratkaisun.

  
**Tietojärjestelmän tulisi pystyä toteuttamaan seuraavanlaisia asioita:**

* Pitämään yksinkertaista kirjarekisteriä jäsenien kirjoista. 
* Jäsenien tulee pystyä merkitsemään kirjasta siihen kuuluvat perustiedot, jotta näillä tiedoilla voidaan myös hakea kirjoja. 
* Kaikkia järjestelmään merkittyjä kirjoja voi lainata.
* Lainausjärjestelmän avulla tulisi tietää kuka omistaa kirjan ja kenellä se on kyseisellä hetkellä lainassa.
* Jäsenet voivat lainata useita kirjoja kerrallaan ja heidän pitää pystyä myös tietämään kirjat, jotka ovat heillä lainassa ja milloin ne pitää palauttaa. 
* Lukutoukat ovat päättäneet, että kirja saa olla lainaushetkestä lähtien enintään 30 päivää lainassa. 
* Kirjoista tulisi myös nähdä niiden lainaushistoria eli milloin ne ovat lainattu.
* Jos kirja on lainassa ja ei ole sillä hetkellä saatavissa niin jäsenen pitäisi pystyä ilmoittamaan itsensä varausjonoon.

Lukutoukat palkitsevat jäseniä aktiivisesta lainaustoiminnasta. He ovat kiinnostuneet myös seuraavanlaisista yhteenvedoista, jotka tulisi saada selville tietokannan avulla.

* TOP 10 lista lainatuista kirjoista ja teoksista koko järjestelmän olemassaolon ajalta.
* Kirjoje ja teoksien määrä tietokannassa sekä erottelu moniko niistä on lainassa tai vapaana.
* Lista erääntyneistä kirjojen ja teoksien palautusajankohdista sekä kenellä kirja on sillä hetkellä lainassa. 

#### Tehtävänäsi on siis suunnitella tarpeeseen sopiva tietokantamalli. Tehtävään ei ole yhtä oikeaa vastausta vaan se vaatii perusteluita valinnoille.



##   

#### Palautus

Palauta perusteltu vastauksesi githubiin seuraavasti aiempien tehtävien tapaisesti.  
  


* Ratkaisun kokeilemista varten oleva .sql tiedosto nimetään tehtävänannon mukaisesti \(015\_tietokannan\_suunnittelu.sql\).
* Tee kuvaus/perustelu Githubin Wiki osioon. Luo sinne siis sivu missä perustelet miten olet päätynyt toteutukseesi. Käytä apuna ER kaavioita ja muita kuvia tarvittaessa. 

Tehtävässä ei haittaa, vaikka kyseiset luontikomennot olisi luotu phpmyadminin avulla tai muulla työkalulla. Tärkeää on, että ohjaaja saa luotua ratkaisun omaan mysql-palvelimeen.  
  
Opiskelijan kannalta tärkeämpää on perusteltu ratkaisu. Kannattaa esimerkiksi kokeilla vierustoverin kanssa, saako hän luotua komennoilla sinun tietokantasi, jotta voit olla varma, että sen luominen onnistuu vaivatta.  
Kun kirjoitat perusteluja niin kirjoita se kuten esittelisit tietokannan rakenteen tuntemattomalle ohjelmoijalle, joka tulee sinun paikallesi. Älä siis typistä asioita liikaa vaan pyri kuvaamaan ratkaisusi selkeästi. Muoto on vapaa. Seuraavaksi on vielä listattu asioita mitä on mahdollista perustella.  
  


* taulun nimi ja mitä se sisältää ja miksi?
* taulujen väliset viiteavaimet sekä pääavaimet. Miksi nämä valittu?
* miten tauluissa on otettu huomuoon normalisointi?
* jne. eli periaattessa se miten olen päässyt kyseiseen ratkaisuun. 

#### Arviointiperusteet

  
**0/Hylätty -&gt;** jos palautusta ei ole tehty palautuspäivään mennessä kun tämä tarkistetaan.  
**1-2 -&gt;** jos ratkaisusta on piirretty opetetun mukainen ER kaavio sekä määritetty pää- ja viiteavaimet. Kyseistä tietokantamallia varten on luotu tarvittavat luontikomennot sekä tietokannan kokeilemista varten esimerkkidata.  
  
**3 -&gt;** edellisten kohtien lisäksi opiskelija on palautuksessaan perustellut miten on päätynyt kyseiseen ratkaisuun.  
  
**4 -&gt;** edellisten lisäksi ratkaisussa on huomioitu normalisointimuodot ja perusteltu niiden käyttö.  
  
**4 - 5 -&gt;** edellisten lisäksi ratkaisussa on huomioitu indeksointi ja perusteltu sen käyttö. Lisäksi opiskelija on voinut näyttää muuta osaamista relaatiotietokantojen käytön osalta.  
  
**Esimerkkidatan sisältö**  
  
- Tällä tarkoitetaan sellaista tietoa, että sillä voi kokeilla tietokannan toimivuuden. Tee siis muutamia lainaajia ja kirjoja tietokantaan.  
- Erityisesti ohjaaja tarkastelee asiakkaan kuvauksessa kerrottuja kohtia tietokannassa ja voiko haluttuja asioita hakea sieltä.  
  
Ps. tehtävässä taulujen määrä ei merkitse. Muista myös, että tehtävästä voi saada haastavan, jos ajattelet liian pitkälle. Ota huomioon käytettävissä oleva aika.  


