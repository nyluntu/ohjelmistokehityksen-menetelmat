# Git perusteet 102

{% hint style="warning" %}
Komennoissa on virheitä kun ne on siirretty tekstiin. Huomaa, että osa komennoista ei siis kopioimalla toimi, joten etsi oikea komento. Virheitä voi olla esimerkiksi väliviivojen kanssa, joiden edestä puuttuu tyhjä välilyönti.
{% endhint %}

Komennoissa on virheitä kun ne on siirretty tekstiin. Huomaa, että osa komennoista ei siis kopioimalla toimi, joten etsi oikea komento. Virheitä voi olla esimerkiksi väliviivojen kanssa, joiden edestä puuttuu tyhjä välilyönti.

**Etätietovarastonviittauksienlisääminen ja poistaminen**

Miten voit lisätä ja poistaa viittauksia etätietovarastoihin?

Paikallinen tietovarasto osoittaa useimmiten myös yhteen etätietovarastooon, jos lähdekoodit jaetaan muiden kehittäjien kanssa.

Millä komennoilla näiden osoitteiden ja viittausten hallinta onnistuu,kun ei käytetä `git clone` –komentoa?

Anna lopuksi komento `git remote–v` ja ota kuvakaappaus, josta näkyy vähintään kaksi eri viittausta etätietovarastoon.

#### Etätietovaraston kehityshaaran hakeminen paikalliseen tietovarastoon <a id="et%C3%A4tietovaraston-kehityshaaran-hakeminen-paikalliseen-tietovarastoon"></a>

Millä komennoilla saat haettua etätietovarastosta erillisen kehityshaaran paikalliseen tietovarastoon?

Kehityshaara ei saa olla siis `master` –kehityshaara vaan jokin muu. Kehityshaara tulee hakea omaan paikalliseen kehityshaaraan ilman, että tapahtuu ns. `merge`.

Kerro vaadittavat komennot ja kuvaile mitä ne tekevät.

#### Etätietovaraston kehityshaaran hakeminen paikalliseen tietovarastoon vetämällä muutokset <a id="et%C3%A4tietovaraston-kehityshaaran-hakeminen-paikalliseen-tietovarastoon-vet%C3%A4m%C3%A4ll%C3%A4-muutokset"></a>

Kysymys on sama kuin edellinen mutta nyt `merge` –tapahtuma saa tapahtua samalla. Kehityshaaran on oltava jokin muu kuin `master` –kehityshaara.

Kerro vaadittavat komennot ja kuvaile mitä ne tekevät.

#### Paikallisten tietovaraston `master` -kehityshaaran työntäminen etätietovarastoon <a id="paikallisten-tietovaraston-master--kehityshaaran-ty%C3%B6nt%C3%A4minen-et%C3%A4tietovarastoon"></a>

Kerro millä komennoilla saat työnnettyä paikallisessa tietovarastossa olevan master-kehityshaaran etätietovarastoon, kun olet ensin siihen tehnyt muutoksia?

#### Paikallisen tietovaraston kehityshaaran tai `tagin` työntäminen etätietovarastoon <a id="paikallisen-tietovaraston-kehityshaaran-tai-tagin-ty%C3%B6nt%C3%A4minen-et%C3%A4tietovarastoon"></a>

Sama idea kuin edellisessä mutta kehityshaaran pitää olla jokin muu kuin master–kehityshaara. Ota kuvakaappaus etätietovarastosta, jossa tämä kehityshaara näkyy. Ota kuvakaappaus etätietovarastosta, josta näkyy sinne merkitty `tag`–merkintä.

