---
tyyppi: kasite
lahteet: [raw/llm-wiki.md]
paivitetty: 2026-11-17
tagit: [llm, tietopankki]
---

# LLM-wiki

Malli henkilökohtaisen tietopankin rakentamiseen: LLM **rakentaa ja ylläpitää inkrementaalisesti pysyvää wikiä** – rakenteista, toisiinsa linkitettyä markdown-tiedostojen kokoelmaa raakalähteiden ja käyttäjän välissä ([[lahde-llm-wiki-idea]]).

## Tunnuspiirteet
- **Pysyvä ja kumuloituva:** tieto koostetaan kerran ja pidetään ajan tasalla, ei johdeta uudelleen joka kysymyksellä (vrt. [[rag]]).
- **LLM kirjoittaa, ihminen lukee:** käyttäjä kuratoi lähteet ja kysyy; LLM hoitaa [[kirjanpito|kirjanpidon]].
- **Kasvaa sekä lähteistä että kysymyksistä:** hyvät vastaukset arkistoidaan takaisin ([[query]]).

## Vertauskuva
[[obsidian]] on IDE, LLM on ohjelmoija, wiki on koodikanta.

## Katso myös
[[kolmen-kerroksen-arkkitehtuuri]] · [[ingest]] · [[lint]] · [[kayttokohteet]] · [[memex]] · [[yleiskatsaus]]
