---
tyyppi: kasite
lahteet: [raw/llm-wiki.md]
paivitetty: 2026-11-17
tagit: [navigointi]
---

# Index ja log

Kaksi erityistiedostoa, joilla on eri tarkoitus ([[lahde-llm-wiki-idea]]).

## index.md – sisällöllinen
- Luettelo kaikista sivuista: linkki, yhden rivin tiivistelmä, valinnaisesti metatietoa (päivämäärä, lähteiden määrä).
- Järjestetty kategorioittain (entiteetit, käsitteet, lähteet…).
- Päivitetään jokaisessa [[ingest]]issä.
- [[query]]ssä luetaan ensin. Toimii yllättävän hyvin ~100 lähteeseen / satoihin sivuihin asti ilman embedding-pohjaista [[rag]]-infraa.

## log.md – kronologinen
- Vain lisättävä tietue: ingestit, kyselyt, [[lint]]-ajot.
- Yhtenäinen etuliite tekee siitä unix-työkaluilla jäsennettävän:
  ```
  ## [2026-04-02] ingest | Artikkelin otsikko
  grep "^## \[" log.md | tail -5
  ```
- Antaa aikajanan wikin kehityksestä ja auttaa LLM:ää näkemään, mitä on tehty viimeksi.

Tämän wikin tiedostot: [[index]] ja [[log]].

## Katso myös
[[qmd]] · [[skeema]]
