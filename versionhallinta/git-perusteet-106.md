---
description: Tavoitteena on oppia tekemään ensimmäinen merkintä versionhallintaan.
---

# Git perusteet 106

## Tavoite

Tehtävän tavoitteena on tehdä ensimmäisiä merkintöjä \(commit\) versionhallintaohjelmalla.

Omalla paikallisella koneellasi, tee sellainen harjoite, jossa sinulla on vähintään 10 merkintää Git lokissa.

Ota kuva lopputuloksesta seuraavalla komennolla:

```bash
git log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```

```text
# Jos haluat edellisen komennon ns. pikakomennoksi niin voit antaa myös seuraavan version komennosta.
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"

# Tämän jälkeen riittää aina seuraava komento.
git lg
```

## Huomioi tehdessä seuraavat asiat

* Aloita tyhjällä Git projektilla. Älä kopioi sitä alkuun mistään.
* Lokista otetussa kuvassa pitää näkyä tekijän nimi. Jos näin ei ole, tee asetukset Gittiin kuntoon.
* Kun teet muutoksen, tee selkeä muutos lähdekoodiin. Tee siis jokin tuttu harjoitus uudelleen.
* Käytä esimerkin kanssa oikeaa projektipohjaa. Esimerkiksi konsoliprojekti Visual Studiossa. Ei yksittäisiä tekstitiedostoja missä ei ole mitään tarkoitusperää.
* Huomioi "commit" viestien kirjoitusasu.
* Mitä komentoja jouduit käyttämään, jotta pääsit tavoitteeseen?
* Mitä "commit" viesteissä kuuluisi lukea?
* Kokeile antaa komento `git commit -m "anna tähän viestisi"`
* Kokeile myös komentoa `git commit` ilman muita parametrejä. Mitä tapahtui ja kuinka selvitit tilanteen?

