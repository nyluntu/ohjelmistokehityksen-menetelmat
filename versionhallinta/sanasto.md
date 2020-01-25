---
description: Sanastoa Git versionhallintaan. Termejä suomeksi ja englanniksi.
---

# Sanasto

{% hint style="info" %}
Sanastossa käytetyt suomenkieliset käännökset eivät ole virallisia käännöksiä. Termit on haettu käyttäen eri lähteitä sekä sitten työelämässä käytetyistä nimityksistä. Virallisia käännöksiä ei sinällään ole.
{% endhint %}

| EN | FI | Selitys |
| :--- | :--- | :--- |
| Repository | Tietovarasto | Tarkoitetaan lähdekoodille luotua varastoa. Voidaan puhua myös eräänlaisesta "git hakemistosta". Sisältää versionhallinnan luoman muutoshistorian lähdekoodista. |
| Remote repository | Etätietovarasto | Tarkoitetaan sellaista olemassa olevaa tietovarasto, joka ei sijaitse kehittäjän työasemalla. Sijaitsee usein erillisellä palvelimella tai palvelussa. \(Esim. Github\) |
| Local repository | Paikallinen tietovarasto | Tarkoitetaan sellaista olemassa olevaa tietovarastoa, joka sijaitsee kehittäjän työasemalla. |
| working directory | Työhakemisto | Tarkoitetaan sitä kansiota missä sillä hetkellä on komentorivillä. Esimerkiksi polku nykyiseen työhakemistoon linux ympäristöissä selviää komennolla `pwd` |
| Reference, remote reference | viittaus | Viittauksella tarkoitetaan Gitin käyttämää tunnistetta, toisinsanoen viittausta esimerkiksi versioihin muutoshistoriassa. Voidaan myös puhua etätietovarastojen viittauksista, joilla tarkoitetaan mihin etätietovarastoon nykyinen paikallinen tietovarasto viittaa. \(Kts. komento `remote`\) |
| Branch | haara, kehityshaara | Tarkoitetaan versionhallinnassa päähaarasta tehtyä sivuhaaraa. Haara voi olla esimerkiksi toisen ominaisuuden takia tehty kopio nykyisestä versiosta, jota kehitetään itsenäisenä kokonaisuutena. Haara voidaan yhdistää takaisin päähaaraan. |
| Tag | Tagi | Tagi on versionhallinnassa käytettävä tunniste, jostakin tietystä versiosta. Tagi voidaan nimetä, joten sen sijaan, että version tunniste on pelkkä SHA1 tunniste, voidaan sille antaa merkittävämpi nimi. |
| Commit | _"Pysyvä muutos"_ | Tarkoitetaan muutosten vahvistamista, jotta ne tulevat voimaan ja näkyvät muutoshistoriassa omalla tunnisteella. |
| Conflict | Konflikti | Tarkoittaa sellaista tilannetta kun työkalu ei osaa yhdistää haluttuja muutoksia esimerkiksi kahden eri kehityshaaran kohdalla. Tällöin syntyy konflikti, jonka kehittäjän on selvitettävä itse ja muokattava alkuperäinen tiedosto haluttuun lopputilaan, joka vahvistetaan. |
| stash | - | Tarkoitetaan Gitin komentoa stash, jolla voidaan kätkeä tai piilottaa hetkellisesti nykyiset voimassa olevat muutokset. |
| staging area | valmistelualue | Yksi Gitin käyttämä tekniikka. Halutut muutokset lisätään aina ennen vahvistamista valmistelualueelle. Kun halutut muutokset ovat koossa, voidaan tehdä pysyvä muutos versionhallinan muutoshistoriaan. |

## Lähteet

{% embed url="https://www.linux.fi/wiki/Git" %}

{% embed url="https://www.cs.helsinki.fi/u/hisahi/sanastot/git\_github.html" %}



