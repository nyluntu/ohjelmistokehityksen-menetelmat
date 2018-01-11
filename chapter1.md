# Git perusteet 101

---

Perusteet luvun tehtävät koostuvat useammasta tasosta. Tasot on yritetty kokoa loogiseen järjestykseen siten, että aina ennen seuraavaa tasoa olisi hyvä tehdä edellinen. Loppupäässä tehtävät ovat kuitenkin vapaampia ja enemmän tiedonhakuun liittyviä, koska joitakin asioita versionhallinnan käytöstä on vaikeampi opettaa suoraan. Erikoistilanteiden luominen opetusta varten on hankalaa ja sen sijaan pyritään tuomaan esille erilaisia tilanteita, joita työskentelyn aikana kohtaa. Monet ovat kuitenkin harvinaisia mutta varsinkin aluksi voi syntyä paljonkin erikoistilanteita mihin ei löydy suoraa vastausta tästä oppaasta.

## TASO 1

Ensisimmäisen tason tehtävien jälkeen tunnet Git -versionhallintatyökalun yleisimpiä komentoja joita tulet tarvitsemaan arkikäytössä.

### Asenna Git tietokoneellesi

Asentamisen jälkeen anna komento `git–version` ja ota kuvakaappaus.

### Konfiguroi Git ensimmäistä käyttökertaa varten

Konfiguroinnin jälkeen anna komento `git config–list` ja ota kuvakaappaus.

### Luo uusi paikallinentietovarastoja ensimmäisen pysyvän muutoksen tekeminen

Tietovaraston luonnin jälkeen lisää muutama tiedosto versionhallinnan jäljitettäväksi ja sen jälkeen tee muutoksista pysyviä. Anna tämän jälkeen komento `git log–stat` ja ota kuvakaappaus.

### Luo paikallinen tietovarasto olemassa olevasta etätietovarastosta

Luo paikallinen kopio seuraavasta julkisesta tietovarastosta:  [https://github.com/nyluntu/hacksummit-forecast](https://github.com/nyluntu/hacksummit-forecast)

Tämän jälkeen anna komento `git remote–v` ja ota kuvakaappaus.

### Nykyisten muutosten tarkistaminen ennen pysyvän muutoksen tekemistä

Mieti millä komennolla näet mitkä tiedostot ovat uusia, poistettuja tai lisätty versionhallinnan jäljitettäväksi, joissa on muutoksia. Tämän jälkeen anna kyseinen Git komento ja ota kuvakaappaus. Kuvakaappauksessa tulisi vähintään näkyä uusi lisätty tiedosto ja yksi tulevaan pysyvään muutokseen lisätty muutos tai jäljitettävä tiedosto.

### Millä komennolla saat lisättyä nykyisestä työkansiosta kaikki muutokset tulevaan pysyvään muutokseen, jos tiedostoja on useampi kuin yksi?

Kerro tähän vaadittavat komennot tai anna muu selitys mitä tulisi tehdä.

### Mitä `git commit` komento tekee?

Kerro vapaamuotoisesti mitä commit–komento tekee käytännössä?

### Miten sivuutan tiedostot, joiden muutoksia en halua jäljitettävän?

Kerro miten sivuutus tapahtuu ja miksi käyttäisit tällaista ominaisuutta? Tarvittaessa ota kuvakaappaus perustelun tueksi.

### Tulevien pysyvien muutosten peruuttaminen

Millä komennolla voit peruuttaa jo valmistellut tiedostot tulevaan pysyvään muutokseen?

Eli olet esimerkiksi muuttanut tiedostoa tai lisännyt uuden jäljitettäväksi mutta huomaat, ettet haluakaan ottaa uutta tiedostoa mukaan seuraavaan pysyvään muutokseen. Muutos on siis jo tässä kohdin **staged** tilassa.

Miten siis peruuttaisit tulevan muutokset, että saat osan tiedostoista pois **staged** tilasta?

Kerro tarvittavat komennot ja ota myös `git status`–komentoa käyttäen pari kuvakaappausta ennen ja jälkeen tilanteen.

### Mitä tekee `git mv` –komento?

Kerro mitä otsikossa mainittu komento tekee ja miksi käyttäisit tai et käyttäisi sitä?

### Mitä tekee `git rm` –komento?

Kerro mitä otsikossa mainittu komento tekee ja miksi käyttäisit tai et käyttäisi sitä?

### Luo oma etätietovarasto ja työnnä sinne muutoksesi

Voit luoda etätietovaraston haluamaasi palveluun. Kun olet muutokset työntänyt tietovarastoon, ota kuva palvelun Git historia-näkymästä sekä sinun paikallisesta historiasta komennolla `git log -10 -oneline`

# Sanasto

// TODO

