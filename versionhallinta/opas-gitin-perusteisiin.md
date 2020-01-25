# Opas Gitin perusteisiin

Versionhallinnan avulla voidaan seurata lähdekoodin muutoksia ja työskennellä tehokkaammin yhdessä. Yksi suosituimmista versionhallintaan suunnitelluista työkaluista on Git. Seuraavassa artikkelissa käydään läpi perusteet, joiden avulla pääset alkuun.

## Yleiskuva Git työkaluun

Git on monipuolinen työkalu, joka on suunniteltu toimimaan hajautettuna versionhallintana \(_distributed version control_\). Hajautettu versionhallinta tarkoittaa sitä, että jokainen kopio Gitin tietovarastosta toimii itsenäisesti. Verrattuna keskitettyihin versionhallintapalveluihin _\(centralized version control\)_, jotka vaativat toimiakseen eräänlaisen keskitetyn tietovaraston muutosten hallintaan, git toimii myös itsenäisesti. Usein kuitenkin myös Git-työkalua käytettäessä mukana on keskitetty tietovarasto, jota käytetään pääasiallisena lähteenä. Hajautettu malli mahdollistaa kuitenkin sen, että monet asiat voidaan tehdä paikallisesti ilman verkkoyhteyttä.

![L&#xE4;hde: Pro Git, Distributed version control.](../.gitbook/assets/image%20%282%29.png)

Etätietovarasto kannattaa ajatella vain kopiona lähdekoodista. Usein sellainen on sijoitettu palvelimelle tai  kolmannen osapuolen palveluun, kuten esimerkiksi Github -palveluun. Etätietovarasto toimii pääosin keskitettynä lähteenä, jossa pidetään lähdekoodin tuorein  versio. Muutoksia ei suoraan tehdä etätietovarastoihin vaan ensin muutokset vahvistetaan paikallisessa tietovarastossa, josta ne sitten työnnetään _\(push\) ****_etätietovarastoon ja ovat koko kehitystiimin saatavilla, joilla vain on pääsy kyseiseen palveluun.

Hajautettu versionhallinta tuo mukanaan myös sellaisen edun, että mikä tahansa tietovaraston kopio voi toimia toisen paikallisen tietovaraston etätietovarastona. Tilanteessa, jossa alkuperäinen etätietovarasto menee vikatilaan tai sitä ei saataisi korjattua, voisi yksi nykyisistä paikallisista tietovarastoista toimia uutena etätietovarastona. Käytännössä tämä tarkoittaa sitä, että yksi kehittäjistä perustaisi uuden etätietovaraston, jonne hän oman muutoshistoriansa työntää. Tällöin kannattaa valita sellainen, jolla on mahdollisimman tuorein muutoshistoria. Tämä toimii siksi, että jokainen tietovaraston kopio sisältää koko päähaaran historian kun se kopioidaan.

Git työkalu käsittelee kaikki muutokset paikallisesti. Muutokset voidaan myös työntää etätietovarastoon _\(remote repository\)_ kun ne tahdotaan jakaa muiden ohjelmoijien kanssa tai sitten muutoin pistää talteen. Karkeasti ottaen Gitin käyttö voidaan jakaa kahteen osa-alueeseen: **paikalliseen tapahtuvaan työskentelyyn** ja **etätietovarastoihin liittyvään työskentelyyn**.

## Gitin kolme tilaa

Ennen tutustumista paikalliseen työskentelyyn, pitää ymmärtää miten Git toimii paikallisesti ja kuinka se käsittelee tiedostojen muutokset. Puhutaan niin sanotusti kolmesta eri tilasta: **työhakemistosta** _\(working directory, workspace\)_, **valmistelualueesta** _\(staging area\)_ ja Git-hakemistosta eli **paikallisesta tietovarastosta** _\(repository\)_. 

![L&#xE4;hde: Pro Git, Working tree, staging area, and Git directory.](../.gitbook/assets/image%20%281%29.png)

### Työhakemisto

Kun työskentelet Git -työkalulla, se käsittelee tietojärjestelmän kansioita ja tiedostoja. Työhakemistolla tarkoitetaan sitä kansiota \(hakemistoa\) mikä on alustettu käyttäen Gitin komentoa tai kloonattu etätietovarastosta. Työhakemistona voi siis toimia mikä tahansa kansio ja komentokehotetta käyttäessä, sillä tarkoitetaan usein juurikin sitä kansiota missä sillä hetkellä on.

Työhakemisto, joka on Gitin seurannassa, toimii kuten normaali kansio. Kun lisäät, muutat tai poistat tiedoston niin Git seuraa näit eroja. Työkalu kertoo missä tilassa tiedostot ovat. Työhakemistossa, jossa Git on käytössä, löytyy aina piilotettu **.git** -niminen kansio \(huomaa piste nimen edessä\) ja sisältää työkalun tarvittavia tiedostoja. Kyseiseen kansioon ei tulisi koskea.

Lähdekoodeihin tehdyt muutokset eivät automaattisesti säily versionhallinnassa vaan Gitin kohdalla pitää kertoa mitkä muutokset halutaan lisätä eli valmistella seuraavaa versiota varten. Tässä termillä versio tarkoitetaan pysyvää muutosta, joka on Gitin lokissa eli muutoshistoriassa. Muutoksen tilalle ei ole väliä vaan lisättiin, poistettiin tai muutettiin tiedostoa niin se tulee aina viedä niin sanotulle valmistelualueelle.

{% hint style="info" %}
Git ei käsittele itseasiassa kansioita vaan pelkkiä tiedostoja. Jos luot siis kansion, joka ei sisällä tiedostoja, ei Git huomaa eroa. Lisää siis aina jokin tiedosto tyhjään kansioon, jos haluat sen pysyvän lähdekoodien mukana jostain syystä.
{% endhint %}

### Valmistelualue

Valmistelualue on eräänlainen välitila ennen pysyvän muutoksen vahvistamista. Valmistelualueelle voidaan lisätä halutut muutokset. Työskentelyn aikana tulee tilanteita, kun ohjelmoija on koskenut useaan tiedostoon mutta haluaa vain lisätä tietyt yksittäiset muutokset eikä kaikkia muutoksia. 

Kun tiedosto lisätään valmistelualueelle, siitä otetaan viimeisin kopio talteen. Tiedoston muuttuessa tämän jälkeen, se pitää lisätä uudelleen valmistelualueelle, joten usein tämä tehdään siinä vaiheessa kun halutut muutokset on tehty. Valmistelualueella ei ole kovin tärkeää osaa päivittäisessä työskentelyssä mutta sen rooli on hyvä tuntea.

Seuraava vaihe on tehdä valmistelualueen tiedostojen kopioista pysyvä versio muutoshistoriaan. Tätä tilannetta kutsutaan _**commitiksi** \(commit\)_, jolloin muutokset vahvistetaan paikalliseen tietovarastoon.

### Paikallinen tietovarasto

Paikallinen tietovarasto on viimeisin kolmesta vaiheesta. Kun pysyvä muutos on tehty, se kirjataan paikalliseen tietovarastoon uutena versiona. Voidaan siis puhua niin sanotusti pysyvästä muutoksesta, josta tulee osa muutoshistoriaa. Samalla kun muutos vahvistuu niin Git merkitsee uusimman muutoksen nykyiseksi version _**"pääksi"**_ _\(HEAD\)_, joka siis viittaa tuoreimpaan versioon.

Muutoshistoria on eräänlainen ketju muutoksia ja sisältää aina tiedon edellisestä versiosta. Eri lähteissä versioista puhutaan myös termillä _snapshot_ eli eräänlaisesta sen hetkisestä tiedostojen tilasta. Pääosin Gitin komennot käsittelevät tätä paikallista tietovarastoa ja etätietovarastojen käsittelyyn varten on omat komentonsa. 

{% hint style="info" %}
Git ei tallenna kopiota koko työhakemistosta \(kuten osa versionhallintaan tehdyistä työkaluista\) kun pysyvä muutos tehdään. Puhutaan enemmän tiedon lisäämisestä eli jokainen muutos kertoo mikä on muuttunut edelliseen versioon nähden. 
{% endhint %}

## Asennus

Asenna Git sen kotisivuilla annettujen ohjeiden mukaisesti. [https://git-scm.com/downloads](https://git-scm.com/downloads)

Esimerkit tehdään käyttäen Git komentoja, jotka suoritetaan komentokehotteen tai terminaalin avulla.

### Ensimmäinen käyttökerta

Konfiguroi Git ensimmäisellä käyttökerralla. Seuraavat kaksi komentoa ovat usein ne tarpeellisimmat, jotka pitää antaa.

```bash
# Asetusten komennot eivät tulosta mitään niiden antamisen jälkeen.
# Tarkoitus on asettaa muutama tieto käyttäjästä, jotta ne näkyvät
# muutoshistoriassa. 

# Asetetaan nimimerkki, jota käytetään muutoshistoriassa.
git config --global user.name "nimesi"

# Asetetaan sähköpostiosoite, jota käytetään muutoshistoriassa.
git config --global user.email "sähköpostiosoite"

# Voit tarkistaa asetukset, jos seuraava komento tulostaa antamasi tiedot.
git config --list | grep user
```

## Paikallisen tietovaraston kanssa työskentely

Gitin kanssa työskentely on melko yksinkertainen prosessi ja samat komennot toistuvat jatkuvasti. Tärkeää on enemmän tietää mitä on tekemässä. Kaikki usein alkaa paikallisesta työskentelystä mikä tarkoittaa sitä, että tehdään muutoksia lähdekoodiin ja vahvistetaan ne paikalliseen tietovarastoon.

Paikallinen työskentely voidaan jakaa seuraaviin pääasiallisiin kokonaisuuksiin: **tietovaraston luominen** ja **muutosten tekeminen**.

### Tietovaraston luominen

Tietovaraston luominen tarkoittaa toimenpidettä missä nykyinen työhakemisto alustetaan käyttämään versionhallintaa, tässä tapauksessa Gittiä. Työhakemiston alustaminen onnistuu alla olevalla komennolla.

Komennon jälkeen työhakemistoon luodaan piilotettu **.git** -kansio. Nyt voit käsitellä työhakemistoa miten olet tottunut eikä se vaikuta normaaliin työskentelyysi.

```bash
# Esimerkissä voidaan olettaa, että työhakemiston polku on:
# C:\repositoryt\GitHarjoitukset\

# Tietovaraston luominen työhakemistoon.
git init
```

{% hint style="info" %}
Tietovaraston luominen tehdään vain kerran. Ei joka kerta kun aloittaa työskentelyn. Jos työhakemistossa on jo **.git** kansio niin tätä vaihetta ei tarvitse tehdä.

Jos paikallinen tietovarasto on alunperin kopioitu etätietovarastosta niin silloinkaan tätä vaihetta ei tarvitse tehdä.

Huomaa myös, että **.git** -kansio on vain usein projektin juuressa. Tarkoittaa sitä, että työhakemistossa olevat alakansiot eivät sisällä piilotettua **.git** -kansiota.

Vältä komennon antamista tietojärjestelmän asemien juuressa, esimerkiksi Windowsissa C:\ -aseman juuressa. Tällöin Git alkaa seuraamaan kaikkia tiedostoja asemalta ja tällöin se ei toimi halutulla tapaa.
{% endhint %}

### Muutoksen tekeminen

Muutoksia tehdessä ne pitää vielä vahvistaa. Seuraavat alla olevat komennot havainnollistavat vaiheita, miten pysyvä muutos paikalliseen tietovarastoon saadaan aikaiseksi. Ohjelmoija toistaa näitä vaiheita jokapäiväisessä työssään jatkuvasti.

```bash
# Esimerkissä voidaan olettaa, että työhakemiston polku on:
# C:\repositoryt\GitHarjoitukset\

# Esimerkin vuoksi voidaan olettaa, että työhakemistoon on lisätty tätä 
# ennen tekstitiedosto "Program.txt", joka sisältää mitä tahansa tekstiä.
# C:\repositoryt\GitHarjoitukset\Program.txt

# Näytä tietovaraston tila
git status

# Lisää kaikki muutokset valmistelualueelle. (komennon lopussa on siis piste)
git add .

# Tee valmistelualueen muutoksista pysyviä nykyiseen kehityshaaraan. 
# Kehityshaara lukee esimerkiksi status -komennon tulosteessa mutta
# tässä kohdin se on nimeltään master.
git commit -m "Minun ensimmäinen commit"
```

Komentojen jälkeen sinulla pitäisi olla tehtynä uusi versio, joka näkyy muutoshistoriassa. Muutoshistoriaa voit katsoa seuraavalla komennolla, jossa sinun pitäisi nähdä tuorein muutoksesi antamasi viestin kera.

```bash
# Esimerkissä voidaan olettaa, että työhakemiston polku on:
# C:\repositoryt\GitHarjoitukset\

# Log komento näyttää muutoshistorian ja parametri -5 tarkoittaa,
# että näyttää edelliset 5 muutosta. Jos komentokehote menee eräänlaiseen
# lukutilaan eikä hyväksy muita painalluksia, paina Q kirjainta.
git log -5
```

{% hint style="info" %}
Esimerkin tilanne voidaan suorittaa myös seuraavalla yksittäisellä komennolla, jos varmasti halutaan kaikki nykyiset muutokset lisätä eikä ole tarvetta tarkistaa sisältöä.

`git commit -a -m "Minun ensimmäinen commit"`

Esimerkissä lisättiin kaikki tiedostot kun käytettiin pistettä. Yksittäisiä tiedostoja voidaan myös lisätä.

`git add Program.txt`
{% endhint %}

## Etätietovaraston kanssa työskentely

Gitin kanssa ei ole pakko käyttää etätietovarastoja mutta usein ne ovat mukana. Tämä voidaan myös jakaa muutamaan pääasialliseen kokonaisuuteen: **tietovaraston kopiointi, etätietovaraston viittauksien muutokset, muutosten työntäminen** ja **muutosten vetäminen.**

### Etätietovaraston kopiointi paikalliseen tietovarastoon

**Tämä vaihe tehdään vain kerran** siinä tilanteessa, että etätietovarasto on jo olemassa ja sitä ei ole nykyisellä työasemalla \(työkoneella\) olemassa vielä. Etätietovarasto on siis perustettu jo toisen henkilön toimesta.

```bash
# Esimerkissä voidaan olettaa, että työhakemiston polku on:
# C:\repositoryt\

# clone komento kopioi sille annetusta URL osoitteesta tietovaraston 
# paikalliseksi tietovarastoksi. Merkit < ja > eivät kuulu komentoon.
# Komennon antamisen jälkeen usein pitää tunnistautua riippuen käytettävästä
# palvelusta.
git clone <osoite git repositoryyn>

# Navigoi komennon jälkeen clone komennon luomaan kansioon.
# cd kansion_nimi
```

Kun etätietovarasto on kopioitu \(kloonattu\) niin `clone`  komento luo etätietovaraston mukaan nimisen kansion työhakemistoon. Se ei siis kopioi tietovarastoa nykyiseen työhakemistoon vaan luo sille alakansion.

{% hint style="info" %}
Clone kopiointi tekee useita vaiheita jo valmiiksi. Esimerkiksi sen jälkeen ei tule enää antaa `git init` komentoa tai tehdä muutoksia etätietovaraston viittaamiseen, koska ne on jo tehty.
{% endhint %}

### Etätietovarastoon viittaaminen paikallisessa tietovarastossa

**Tämä vaihe tehdään vain kerran siinä tilanteessa**, että etätietovarastoa ei kopioida \(kloonata\) vaan on kyseessä paikallinen tietovarasto. Tässä tilantessa usein halutaan kertoa mihin etätietovarastoon olemassaoleva paikallinen tietovarasto halutaan työntää. 

Muita tilanteita ovat esimerkiksi sellaiset, että paikallinen tietovarasto muutoshistorian kanssa halutaan työntää toiseen uuteen etätietovarastoon. Käyttötapauksia on monenlaisia.

```bash
# Esimerkissä voidaan olettaa, että työhakemiston polku on:
# C:\repositoryt\GitHarjoitukset\

# Anna työhakemistossa alla oleva komento, joka lisää viittauksen 
# etätietovarastoon. Origin on tässä vapaavalintainen etätietovaraston
# nimi, jota tarvitaan muutoksia työntäessä myöhemmin. Origin on aina
# usein oletuksena annettu nimi.
git remote add origin <osoite git repositoryyn>

# Tarkista komennon antamisen jälkeen, että näet lisätyn viittauksen 
# seuraavan komennon avulla.
git remote -v
```

### Muutosten työntäminen etätietovarastoon

Kun työskentelyssä on tultu siihen pisteeseen, että muutokset halutaan jakaa muiden kehittäjien kanssa tai muutoin talteen eri sijaintiin niin tarvitsee ne työntää \(push\) etätietovarastoon. Tätä vaihetta tehdään niin usein kun on tarve mutta usein päivän päätteeksi.

On hyvä huomioida, että edelliset komennot ovat pääasiassa käsitelleet paikallista tietovarastoa ja seuraavat komennot käsittelevät etätietovarastoa.

```bash
# Esimerkissä voidaan olettaa, että työhakemiston polku on:
# C:\repositoryt\GitHarjoitukset\

# Anna työhakemistossa alla oleva komento. Komento työntää paikallisessa
# tietovarastossa olevat uudet muutokset etätietovarastoon. Jos uusia ei 
# ole niin komento kertoo kaiken olevan ajantasalla. Origin on viittaus
# etätietovarastoon ja master on päähaara, jota tässä ollaan lisäämässä.
git push origin master
```

Yksinkertaisesti `push` komento työntää aina muutokset etätietovarastoon. Tämän jälkeen paikalliseen tietovarastoon voidaan tehdä lisää muutoksia ja työntää taas uudelleen kun halutaan.

{% hint style="info" %}
Push komento voi tietyissä tilanteessa epäonnistua. Todennäköisin tilanne on se kun toinen henkilö on jo ehtinyt työntää uusia muutoksia etätietovarastoon, joita sinun paikallisessa tietovarastossa ei ole. Tässä tilanteessa muutokset pitää ensin vetää omaan tietovarastoon.
{% endhint %}

### Muutosten vetäminen etätietovarastosta

Työskentelyyn saattaa usein liittyä useampi ohjelmoija, jotka tekevät muutoksia. Tuoreet muutokset pitää vetää \(pull\) etätietovarastosta paikalliseen tietovarastoon siinä tilanteessa kun pitää saada muiden muutokset työasemalle. 

```bash
# Esimerkissä voidaan olettaa, että työhakemiston polku on:
# C:\repositoryt\GitHarjoitukset\

# Anna työhakemistossa alla oleva komento. Komento vetää uusimmat muutokset
# etätietovarstosta, joita paikallisessa tietovarastossa ei ole.
# Pull komento tekee myös ns. mergen eli yhdistää ne paikallisen tietovaraston
# muutoshistoriaan.
git pull origin master
```

{% hint style="info" %}
Pull komento on hyvä tehdä aina ennen töiden aloittamista niin välttää monia ongelmatilanteita vanhentuneen lähdekoodin vuoksi.

Komento voi aiheuttaa myös niin sanotun konfliktin \(conflict\) tilanteen, jos vedettävät muutokset koskettavat sellaisia paikallisia muutoksia mitkä osuvat samoihin tiedostoihin ja lähdekoodin riveihin.
{% endhint %}

## Lähteet

{% embed url="https://git-scm.com/" %}

{% embed url="https://fi.wikipedia.org/wiki/Versiohallinta" %}

{% embed url="https://git-scm.com/book/en/v2" %}





