---
tyyppi: kasite
lahteet: [raw/llm-wiki.md]
paivitetty: 2026-11-17
tagit: [arkkitehtuuri]
---

# Kolmen kerroksen arkkitehtuuri

[[llm-wiki]]n rakenne ([[lahde-llm-wiki-idea]]):

| Kerros | Sisältö | Omistaja | Muokattavuus |
|---|---|---|---|
| **Raakalähteet** | Artikkelit, paperit, kuvat, datatiedostot | Käyttäjä kuratoi | Muuttumaton – totuuden lähde |
| **Wiki** | Tiivistelmät, entiteetti- ja käsitesivut, vertailut, yleiskatsaus, synteesi | LLM | LLM luo ja päivittää |
| **[[skeema]]** | Rakenne, konventiot, työnkulut | Yhdessä | Kehittyy ajan myötä |

Tässä wikissä: `raw/`, `wiki/` ja `CLAUDE.md`.

## Katso myös
[[ingest]] · [[query]] · [[lint]] · [[index-ja-log]]
