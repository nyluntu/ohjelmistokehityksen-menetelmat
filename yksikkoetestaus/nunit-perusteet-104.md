# NUnit perusteet 104

## **FizzBuzz -ohjelman toteuttaminen yksikkötestein**

Tutustutaan klassikoksi muodostuneeseen ohjelmointiongelmaan:

> Kirjoita ohjelma, joka kysyy käyttäjältä lukua yhden ja sadan väliltä ja tulostaa luvun. Jos luku on kolmella jaollinen, luvun sijaan tulostetaan "Fizz". Jos luku on viidellä jaollinen, luvun sijaan tulostetaan "Buzz". Jos luku on sekä kolmellä että viidellä jaollinen, luvun sijaan tulostetaan "FizzBuzz".

Ohjelma voi olla sinulle tuttu. Nyt tavoitteena on tehdä ohjelma ensin yksikkötestien kanssa ja vasta lopuksi toteuttaa konsoliohjelma syötteiden kysymiseen. 

Tarkoituksena on oppia erottamaan testikoodi niin sanotusta tuotantokoodista. Yritä, että saisit testien avulla varmistettua ensin ohjelman toimivuuden. 

Ohjelman toimivuuden todentamiseksi riittää toteutetut testit. Konsoliprojektia ei tarvitse välttämättä olla, jos et halua vielä sellaista lisätä.

```text
# Esimerkki mitä ohjelman tulisi tehdä kun sille annetaan lukuja 1-100 väliltä.
# Huomaa, että testaan usealla luvulla, jotta se varmasti käyttäytyy oikein.

1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz
... aina lukuun 100 asti.
```

{% hint style="info" %}
Tehtävänannossa puhutaan tarkoituksella, että käyttäjä antaa syötteen. Lopullisen ohjelman tulisi toimia tällä tavoin mutta sinun tehtäväsi on pohtia, miten esimerkiksi käyttäjän syöte tulee huomioitua testeissä. Tarvitseeko sitä edes testata?
{% endhint %}

## Vinkkejä matkan varrelle

Harjoitus ei ole ohjaajan luoma vaan siihen löytyy useita ratkaisuehdotuksia. Pyri kuitenkin ensin itse ratkaisemaan ongelma ja vasta sitten tarvittaessa hae apua.

Ratkaise logiikka ensin paperilla. Kokeile miettiä miten ohjelman tulee toimia ja vasta sitten siirry ohjelmoinnin pariin.

Jos testit eivät onnistu ensimmäisenä niin ratkaise se ensin ilman niitä. Lisää sitten vasta testit.

Pilko ongelma pienempiin palasiin... lähde helpoimmasta päästä testaamaan eli arvosta 1. Sitten yksi kerrallaan kokeile erilaiset tilanteet läpi. Tarkoitus ei ole käydä kaikkia 100 lukua läpi vaan vain sen verran, että ohjelman voi todeta toimivan.

