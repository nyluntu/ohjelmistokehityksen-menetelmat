# Git perusteet 101

{% hint style="warning" %}
Komennoissa on virheitä kun ne on siirretty tekstiin. Huomaa, että osa komennoista ei siis kopioimalla toimi, joten etsi oikea komento. Virheitä voi olla esimerkiksi väliviivojen kanssa, joiden edestä puuttuu tyhjä välilyönti.
{% endhint %}

**Asenna Git tietokoneellesi**

Asentamisen jälkeen anna komento `git–version` ja ota kuvakaappaus.

#### Konfiguroi Git ensimmäistä käyttökertaa varten <a id="konfiguroi-git-ensimm%C3%A4ist%C3%A4-k%C3%A4ytt%C3%B6kertaa-varten"></a>

Konfiguroinnin jälkeen anna komento `git config–list` ja ota kuvakaappaus.

#### Luo uusi paikallinentietovarastoja ensimmäisen pysyvän muutoksen tekeminen <a id="luo-uusi-paikallinentietovarastoja-ensimm%C3%A4isen-pysyv%C3%A4n-muutoksen-tekeminen"></a>

Tietovaraston luonnin jälkeen lisää muutama tiedosto versionhallinnan jäljitettäväksi ja sen jälkeen tee muutoksista pysyviä. Anna tämän jälkeen komento `git log–stat` ja ota kuvakaappaus.

#### Luo paikallinen tietovarasto olemassa olevasta etätietovarastosta <a id="luo-paikallinen-tietovarasto-olemassa-olevasta-et%C3%A4tietovarastosta"></a>

Luo paikallinen kopio seuraavasta julkisesta tietovarastosta: [https://github.com/nyluntu/hacksummit-forecast](https://github.com/nyluntu/hacksummit-forecast)

Tämän jälkeen anna komento `git remote–v` ja ota kuvakaappaus.

#### Nykyisten muutosten tarkistaminen ennen pysyvän muutoksen tekemistä <a id="nykyisten-muutosten-tarkistaminen-ennen-pysyv%C3%A4n-muutoksen-tekemist%C3%A4"></a>

Mieti millä komennolla näet mitkä tiedostot ovat uusia, poistettuja tai lisätty versionhallinnan jäljitettäväksi, joissa on muutoksia. Tämän jälkeen anna kyseinen Git komento ja ota kuvakaappaus. Kuvakaappauksessa tulisi vähintään näkyä uusi lisätty tiedosto ja yksi tulevaan pysyvään muutokseen lisätty muutos tai jäljitettävä tiedosto.

#### Millä komennolla saat lisättyä nykyisestä työkansiosta kaikki muutokset tulevaan pysyvään muutokseen, jos tiedostoja on useampi kuin yksi? <a id="mill%C3%A4-komennolla-saat-lis%C3%A4tty%C3%A4-nykyisest%C3%A4-ty%C3%B6kansiosta-kaikki-muutokset-tulevaan-pysyv%C3%A4%C3%A4n-muutokseen-jos-tiedostoja-on-useampi-kuin-yksi"></a>

Kerro tähän vaadittavat komennot tai anna muu selitys mitä tulisi tehdä.

#### Mitä `git commit` komento tekee? <a id="mit%C3%A4-git-commit-komento-tekee"></a>

Kerro vapaamuotoisesti mitä commit–komento tekee käytännössä?

#### Miten sivuutan tiedostot, joiden muutoksia en halua jäljitettävän? <a id="miten-sivuutan-tiedostot-joiden-muutoksia-en-halua-j%C3%A4ljitett%C3%A4v%C3%A4n"></a>

Kerro miten sivuutus tapahtuu ja miksi käyttäisit tällaista ominaisuutta? Tarvittaessa ota kuvakaappaus perustelun tueksi.

#### Tulevien pysyvien muutosten peruuttaminen <a id="tulevien-pysyvien-muutosten-peruuttaminen"></a>

Millä komennolla voit peruuttaa jo valmistellut tiedostot tulevaan pysyvään muutokseen?

Eli olet esimerkiksi muuttanut tiedostoa tai lisännyt uuden jäljitettäväksi mutta huomaat, ettet haluakaan ottaa uutta tiedostoa mukaan seuraavaan pysyvään muutokseen. Muutos on siis jo tässä kohdin **staged** tilassa.

Miten siis peruuttaisit tulevan muutokset, että saat osan tiedostoista pois **staged** tilasta?

Kerro tarvittavat komennot ja ota myös `git status`–komentoa käyttäen pari kuvakaappausta ennen ja jälkeen tilanteen.

#### Mitä tekee `git mv` –komento? <a id="mit%C3%A4-tekee-git-mv-%E2%80%93komento"></a>

Kerro mitä otsikossa mainittu komento tekee ja miksi käyttäisit tai et käyttäisi sitä?

#### Mitä tekee `git rm` –komento? <a id="mit%C3%A4-tekee-git-rm-%E2%80%93komento"></a>

Kerro mitä otsikossa mainittu komento tekee ja miksi käyttäisit tai et käyttäisi sitä?

#### Luo oma etätietovarasto ja työnnä sinne muutoksesi <a id="luo-oma-et%C3%A4tietovarasto-ja-ty%C3%B6nn%C3%A4-sinne-muutoksesi"></a>

Voit luoda etätietovaraston haluamaasi palveluun. Kun olet muutokset työntänyt tietovarastoon, ota kuva palvelun Git historia-näkymästä sekä sinun paikallisesta historiasta komennolla `git log -10 -oneline`

## Sanasto <a id="sanasto"></a>

// TODO

