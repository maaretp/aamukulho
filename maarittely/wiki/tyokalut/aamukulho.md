---
tyyppi: tyokalu
lahteet: [../OMINAISUUDET.md, ../README.md]
paivitetty: 2026-11-17
tagit: [aamiainen, oma-sovellus, pwa, budjetti]
---

# Aamukulho (oma sovellus)

Oma aamiaissovellus: "Terveellinen aamiainen joka päivä, alle eurolla ja muutamassa minuutissa." Se on yksi HTML-tiedosto ilman riippuvuuksia ja toimii PWA:na (manifest + service worker). Lähteet: `../OMINAISUUDET.md`, `../README.md` (sovelluskansion dokumentaatio, ei `raw/`-lähde).

## Ominaisuudet
- **12 helppoa aamiaista** marketin aineksista. Jokaisesta näkyy valmistusaika, hinta per annos ja proteiini. Nopein on valmis 3 minuutissa.
- **Pikasuodattimet:** alle 5 min, valmista etukäteen, proteiinia 15 g+, alle 0,70 €.
- **Viikkosuunnitelma:** syötetään budjetti ja syöjien määrä. "Täytä viikko" laittaa arkiaamuille nopeat ja viikonloppuun rauhallisemmat aamiaiset. Jos budjetti ylittyy, kalleimmat päivät vaihtuvat automaattisesti halvempiin.
- **Budjettipalkki** ja hinta per henkilö per päivä (tyypillisesti 0,50–0,90 €).
- **Ostoslista:** henkilömäärän mukaan, ryhmitelty kaupan osastoihin, rastit, kaapista yleensä löytyvät erikseen.
- **Sunnuntain valmistelulista:** noin 20 minuuttia (munat, granola, tuorepuurot).
- **Vinkit:** halvat terveelliset raaka-aineet, mitä tehdä kun aamu menee pieleen, peruskaapin lista hintoineen.
- **Piirroskuvat (ei tekoälykuvia)** ja mahdollisuus lisätä oma valokuva.
- **Alusta:** kotinäytölle, ei rekisteröitymistä, ei mainoksia, tumma tila, valikko peukalon ulottuvilla, offline (vaatii https). Data on vain laitteen `localStorage`ssa.

## Mitä ei (vielä) ole
Ei ruokavalio- tai allergiasuodattimia, ei hakua, ei jakamista, ei synkronointia laitteiden välillä, ei omia reseptejä käyttöliittymästä (vain koodiin), ei kokkaustilaa, ei muistutuksia. Vertailu kilpailijoihin: [[aamukulho-erottautuminen]].

## Katso myös
[[aamiaissovellukset]] · [[aamiaisen-erityispiirteet]] · [[aamukulho-erottautuminen]] · [[lahde-aamiaissovellukset-ominaisuudet]]
