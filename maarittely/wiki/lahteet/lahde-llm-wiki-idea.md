---
tyyppi: lahde
lahteet: [raw/llm-wiki.md]
paivitetty: 2026-11-17
tagit: [llm, tietopankki, ideadokumentti]
---

# Lähde: LLM Wiki (ideadokumentti)

**Tiedosto:** `raw/llm-wiki.md`
**Laji:** "Idea file" – tarkoitettu kopioitavaksi omalle LLM-agentille (Codex, Claude Code, OpenCode/Pi…), joka rakentaa yksityiskohdat yhdessä käyttäjän kanssa. Kuvaa mallin, ei toteutusta.

## Tiivistelmä

Dokumentti esittää [[llm-wiki]]-mallin: sen sijaan että LLM hakisi raakadokumenteista joka kysymyksellä ([[rag]]), se rakentaa ja ylläpitää pysyvää, toisiinsa linkitettyä markdown-wikiä lähteiden ja käyttäjän välissä.

## Pääkohdat

1. **Kumuloituminen.** Uusi lähde integroidaan: entiteettisivut päivitetään, aihetiivistelmät tarkistetaan, ristiriidat merkitään, synteesi vahvistuu tai haastetaan.
2. **Roolit.** Käyttäjä ei (juuri) kirjoita wikiä. Hän hankkii lähteet, tutkii ja kysyy; LLM summaa, ristiviittaa ja arkistoi. Kirjoittaja käyttää rinnakkain LLM-agenttia ja [[obsidian]]ia.
3. **Arkkitehtuuri:** [[kolmen-kerroksen-arkkitehtuuri]] – raw / wiki / [[skeema]].
4. **Toiminnot:** [[ingest]], [[query]], [[lint]].
5. **Navigointi:** [[index-ja-log]]; lokimerkinnät yhtenäisellä etuliitteellä grepattaviksi.
6. **Valinnaiset työkalut:** [[qmd]] hakuun; vinkit [[obsidian-web-clipper]], kuvien lataus paikallisesti, graph view, [[marp]], [[dataview]], [[git]].
7. **Miksi toimii:** [[kirjanpito]] on se, mikä tappaa wikit; LLM ei kyllästy.
8. **Esikuva:** [[memex]].
9. **Käyttökohteet:** ks. [[kayttokohteet]].

## Huomioita

- Dokumentti korostaa itse olevansa tarkoituksella abstrakti: kaikki on valinnaista ja modulaarista.
- Kuvat: LLM ei lue markdownia ja sen inline-kuvia yhdellä kertaa – luetaan ensin teksti, sitten kuvat erikseen.
- Mittakaava-arvio: indeksitiedosto riittää ~100 lähteeseen / satoihin sivuihin.

## Katso myös
[[yleiskatsaus]] · [[index]]
