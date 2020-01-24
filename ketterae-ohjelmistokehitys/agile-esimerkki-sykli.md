# Agile esimerkki, sykli

Esimerkissä on kuvattu yksittäisen syklin \(sprintti, vaihe, sykli, iteraatio jne.\) kierto ja mitä se sisältää. Syklin sisältö on kerätty omien kokemusten perusteella ja se saattaa yhdistellä useita eri menetelmiä. Tarkoituksena on kuitenkin antaa esimerkki ja sen kautta harjoitusprojektin yhteydessä noudattaa ohjeistettua tapaa.

![Viitattu 1.2.2019, Smashing Magazine, Fitting Big-Picture UX Into Agile Development \[1\]](../.gitbook/assets/designsprint.png)

### Vaatimusmäärittely <a id="vaatimusm%C3%A4%C3%A4rittely"></a>

**Käyttäjätarina -kuvaus**

* [User Stories](https://www.agilealliance.org/glossary/user-stories)
* [Advantages of User Stories for Requirements](http://www.mountaingoatsoftware.com/articles/advantages-of-user-stories-for-requirements)
* [Role-Feature-Reason](https://www.agilealliance.org/glossary/role-feature/)

Käytämme käyttäjätarinoihin Role-Feature-Reason tapaista kuvausta. Syvempi kuvaus ei ole tässä kohdin tärkeä vaan yritetään ensin muodostaa ymmärrettävä lause, joka muodostuu mallin mukaisesti.

Usein tarkempi määrittely ja kuvaus voidaan kirjoittaa ennen tarinan toteuttamista tai jopa ennen sitä suunnitteluvaiheessa, jossa mukana on henkilö, joka tuntee tämän tarinan sisällön. Liian tarkkaan ei tarvitse määritellä vaan pystyä tekemään kuvaus, jolla priorisoidaan tarve. Käyttötapauksia voidaan hyödyntää toteuttamisvaiheen alussa ja tehdä tarkempi suunnitelma miten ominaisuudet toimivat.

**Käyttötapaus -kuvaus**

* Kts. User Stories linkki
* [Requirements 1010: User Stories vs. Use Cases](http://www.stellman-greene.com/2009/05/03/requirements-101-user-stories-vs-use-cases/)
* [User Stories Versus Use Cases](https://www.scrumalliance.org/community/articles/2015/october/user-stories-vs-use-cases)
* [Basic Use Case template, Alistair Cockburn](http://alistair.cockburn.us/Basic+use+case+template)

Käyttötapaus on dokumentti mikä voidaan kirjoittaa esimerkiksi käyttäjätarinan perusteella. Huomaa lähteissäkin, että ne pyrkivät kertomaan mikä ero on käyttäjätarinalla ja käyttötapauksella. Lyhyesti, käyttötapaus voidaan nähdä tarkempana määritelmänä miten ohjelma kommunikoi eri osapuolten kanssa ja toteuttaa halutun tavoitteen.

**Tuotteen -backlog**

* [Backlog](https://www.agilealliance.org/glossary/backlog/)
* [Product Backlog](http://www.scrumguides.org/scrum-guide.html#artifacts-productbacklog)
* [Grooming Backlog](https://www.agilealliance.org/glossary/backlog-grooming/)

Tuotteen tehtävälista on dokumentti, joka ohjaa kehitystä. Se muuttuu aika ajoin ja pääasiassa tuotteen omistaja huolehtii siitä. Kehitystiimi kuitenkin osallistuu tähän myös tarvittaessa ja varsinkin kun tehtäviä otetaan seuraavaan sykliin.

**Syklin \(sprintin\) -backlog**

* [Sprint Backlog](http://www.scrumguides.org/scrum-guide.html#artifacts-sprintbacklog)

Syklin tehtävälista on dokumentti, johon on valittu ne tehtävät mitkä kehitystiimi "lupaa" tehdä. Tarkoitus on, ettei valita liikaa vaan voidaan melko tarkasti sanoa, että ne toteutuvat. Tehtäviä katsotaan läpi aina syklien lopussa ja siivotaan sekä korjataan olettamuksia.

### Ohjelmointi <a id="ohjelmointi"></a>

**Versionhallinta**

* Kts. Versionhallinan perusteet

**Yksikkötestaus ja TDD**

* Kts. yksikkötestauksen perusteet
* Kts. yksikkötestauksen perusteet

**SOLID -sääntö/ohje**

* [Wikipedia: SOLID](https://en.wikipedia.org/wiki/SOLID_%28object-oriented_design%29)
* [SOLID architecture principles using simple C\# examples](https://www.codeproject.com/Articles/703634/SOLID-architecture-principles-using-simple-Csharp)
* [Robert Martin SOLID Principles of Object Oriented and Agile Design \(video\)](https://www.youtube.com/watch?v=TMuno5RZNeE)

SOLID säännöstä ei ole muuta kirjoitettua materiaalia tässä kirjassa. Lähteet auttavat sinua tutustumaan aiheeseen ja varsinkin Robert Martinin video on valaiseva. Kyseinen henkilö on säännön luonut eri kokemuksien pohjalta. Säännön tarkoitus on koostaa hyviä tapoja olio-ohjelmoinnin luokkien ohjelmointiin ja parantaa koodin laatua. Käytännössä on kyse ohjelmoinnista ja vain vinkata mitä huomioida kun ohjelman koodia tuotetaan ja kuinka se auttaa myöhemmin muutosten tekemisessä.

### Syklin lopetus <a id="syklin-lopetus"></a>

**Tuoteversio \(Increment\)**

* Kts. Scrum guide ja etsi sana increment.
* [Sprint Review](http://www.scrumguides.org/scrum-guide.html#events-review)
* [Sprint Retrospective](http://www.scrumguides.org/scrum-guide.html#events-retro)

Lyhyesti tarkoitetaan sitä, että kehitystiimi on lisännyt tuotteeseen ominaisuuksia, jotka tarvittaessa tuotteen omistajan hyväksymisen jälkeen voidaan julkaista. Julkaisu ei ole pakollinen vaan isompi julkaisu voidaan tehdä useammassa syklissä. Tärkeintä on, että tuote on aina julkaisuvalmis tarvittaessa, koska välttämättä kaikkien ominaisuuksien ei tarvitse olla valmiita. Tämä on ketterän ohjelmistokehityksen tavoite. Tehdä vähän, julkaista ja oppia tuotteesta. Tällöin riskit voidaan rajat esimerkiksi 2 viikon jaksoihin kuukausien sijasta.

![](../.gitbook/assets/communication.jpeg)

## Lähteet

\[1\] [https://www.smashingmagazine.com/2012/11/design-spikes-fit-big-picture-ux-agile-development/](https://www.smashingmagazine.com/2012/11/design-spikes-fit-big-picture-ux-agile-development/)

