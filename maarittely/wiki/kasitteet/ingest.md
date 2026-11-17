---
tyyppi: kasite
lahteet: [raw/llm-wiki.md]
paivitetty: 2026-11-17
tagit: [toiminto]
---

# Ingest

Uuden lähteen käsittely ([[lahde-llm-wiki-idea]]). Käyttäjä lisää lähteen raakakokoelmaan ja pyytää LLM:ää käsittelemään sen.

## Esimerkkikulku
1. LLM lukee lähteen.
2. Keskustelee pääkohdista käyttäjän kanssa.
3. Kirjoittaa tiivistelmäsivun wikiin.
4. Päivittää indeksin ([[index-ja-log]]).
5. Päivittää relevantit entiteetti- ja käsitesivut koko wikissä.
6. Lisää merkinnän lokiin.

Yksi lähde voi koskettaa **10–15 wikisivua**.

## Tyylit
- **Yksi kerrallaan, osallistuen** – kirjoittajan suosima: lukee tiivistelmät, tarkistaa päivitykset, ohjaa painotuksia.
- **Eräajo** – monta lähdettä kerralla vähemmällä valvonnalla.

Valittu tyyli kirjataan [[skeema]]an.

## Katso myös
[[query]] · [[lint]] · [[obsidian-web-clipper]]
