---
tyyppi: yleiskatsaus
lahteet: [raw/llm-wiki.md, raw/aamiaissovellukset/ominaisuudet.md]
paivitetty: 2026-11-17
---

# Yleiskatsaus

Wikissä on kaksi aihetta: **[[llm-wiki]]-malli** eli wikin oma toimintatapa ([[lahde-llm-wiki-idea]]) ja oman **[[aamukulho]]-aamiaissovelluksen** tuotekehitys suhteessa kilpailijoihin ([[lahde-aamiaissovellukset-ominaisuudet]]).

## Nykyinen synteesi

- **Ydinero [[rag]]-malliin:** RAG löytää ja yhdistelee tiedon uudelleen jokaisella kysymyksellä. LLM-wikissä tieto *koostetaan kerran ja pidetään ajan tasalla* – ristiviittaukset, ristiriidat ja synteesi ovat valmiina. Wiki on kumuloituva artefakti.
- **Rakenne:** [[kolmen-kerroksen-arkkitehtuuri]] – muuttumattomat raakalähteet, LLM:n omistama wiki ja [[skeema]], joka ohjaa LLM:ää.
- **Toiminnot:** [[ingest]] (lähteen integrointi, koskettaa usein 10–15 sivua), [[query]] (vastaukset voi arkistoida takaisin wikiin) ja [[lint]] (terveystarkastus).
- **Navigointi:** [[index-ja-log]] riittää kohtuulliseen mittakaavaan (~100 lähdettä, satoja sivuja) ilman embedding-infraa; isommassa mittakaavassa hakutyökalu kuten [[qmd]].
- **Miksi toimii:** ihmiset hylkäävät wikit, koska [[kirjanpito]] kasvaa nopeammin kuin arvo. LLM:lle ylläpidon kustannus on lähes nolla.
- **Roolijako:** ihminen kuratoi lähteet, ohjaa analyysia ja kysyy; LLM tekee kaiken muun. Vertauskuva: [[obsidian]] on IDE, LLM ohjelmoija, wiki koodikanta.
- **Historia:** idea muistuttaa [[memex]]iä (1945) – Bushilta puuttui vain ratkaisu ylläpitäjäksi.

## Aamukulho ja kilpailijat
- **Kilpailukenttä:** 12 Google Play -sovellusta ([[aamiaissovellukset]]). Puhtaat aamiaissovellukset ovat reseptikirjoja, ja yleiset suunnittelijat kohtelevat aamiaista yhtenä ateriana muiden joukossa.
- **Aamukulhon ainutlaatuinen kärki:** hinta per annos ja viikkobudjetti, jossa kalleimmat päivät vaihtuvat automaattisesti halvempiin (kukaan kilpailija ei mainitse tätä), suomalainen marketti, ei tiliä ja koottu sunnuntain valmistelulista.
- **Aukot:** ruokavalio- ja allergiasuodattimet, jakaminen, haku raaka-aineella, omat reseptit.
- **Vapaa tila:** aamurutiiniin ja kalenteriin kytkeytyvät muistutukset sekä toistuvan vakioaamiaisen pikavalinta ([[aamiaisen-erityispiirteet]]).
- **Suositus:** erottua rutiinilla, rahalla ja rauhalla, ei määrällä. Ks. [[aamukulho-erottautuminen]].

## Avoimet kysymykset
- Kilpailijadata on markkinointitekstiä. Käyttäjäarviot (Play-kommentit) kertoisivat todelliset kipupisteet.
- Kuinka tarkasti Aamukulhon hinnat vastaavat nykyisiä kauppahintoja, ja miten niitä ylläpidetään?
- Ingestoidaanko lähteet yksi kerrallaan keskustellen vai eräajona?

## Katso myös
[[index]] · [[log]] · [[aamukulho-erottautuminen]]
