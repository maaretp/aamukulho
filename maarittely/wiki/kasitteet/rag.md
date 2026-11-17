---
tyyppi: kasite
lahteet: [raw/llm-wiki.md]
paivitetty: 2026-11-17
tagit: [llm, haku]
---

# RAG (retrieval-augmented generation)

Tavallisin tapa käyttää LLM:ää dokumenttien kanssa: kokoelma ladataan, LLM hakee kyselyhetkellä relevantit palat ja generoi vastauksen. Esimerkkejä: NotebookLM, ChatGPT:n tiedostolataukset ([[lahde-llm-wiki-idea]]).

## Rajoitus
LLM **löytää tiedon uudelleen joka kysymyksellä** – mitään ei kerry. Hienovarainen, viittä dokumenttia yhdistelevä kysymys vaatii palojen etsimisen ja kokoamisen joka kerta alusta.

## Suhde LLM-wikiin
[[llm-wiki]] koostaa tiedon etukäteen. Kohtuullisessa mittakaavassa [[index-ja-log|indeksi]] korvaa embedding-pohjaisen RAG-infran; isompana avuksi hakutyökalu kuten [[qmd]].

## Katso myös
[[yleiskatsaus]] · [[query]]
