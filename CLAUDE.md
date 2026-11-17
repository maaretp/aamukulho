# LLM-wiki – skeema

Tämä hakemisto on LLM:n ylläpitämä henkilökohtainen tietopankki ([[llm-wiki]]-malli). Ihminen kuratoi lähteet ja kysyy; LLM kirjoittaa ja ylläpitää wikin.

## Rakenne

Wiki sijaitsee kansiossa `maarittely/` (sovelluksen repossa). Kaikki tämän skeeman polut ovat suhteessa siihen.

- `raw/` – alkuperäiset lähteet. **Muuttumattomia**: lue, älä koskaan muokkaa. Kuvat `raw/assets/`.
- `wiki/` – LLM:n omistama kerros.
  - `index.md` – sisällysluettelo: jokainen sivu linkkinä + yhden rivin tiivistelmä, kategorioittain.
  - `log.md` – kronologinen, vain lisättävä loki.
  - `yleiskatsaus.md` – koko wikin synteesi; päivitetään kun kokonaiskuva muuttuu.
  - `lahteet/` – yksi tiivistelmäsivu per lähde.
  - `kasitteet/` – käsite- ja aihesivut.
  - `tyokalut/` – työkalut, tuotteet, ohjelmistot.
  - `vastaukset/` – tallennetut query-vastaukset (vertailut, analyysit).
  - Uusia kansioita (esim. `henkilot/`, `vastaukset/`) saa luoda tarpeen mukaan; lisää ne tähän skeemaan.

## Sivujen konventiot

- Kieli: suomi. Erisnimet ja vakiintuneet termit (RAG, ingest, lint) alkuperäisinä.
- Tiedostonimet: pienet kirjaimet, väliviivat, ei ääkkösiä (`ingest.md`, `obsidian-web-clipper.md`). Nimet ovat koko wikissä yksilöllisiä.
- Linkit Obsidian-muodossa: `[[tiedostonimi]]` tai `[[tiedostonimi|näkyvä teksti]]`.
- Jokaisessa sivussa YAML-frontmatter:
  ```yaml
  ---
  tyyppi: lahde | kasite | tyokalu | yleiskatsaus | vastaus
  lahteet: [raw/tiedosto.md]
  paivitetty: VVVV-KK-PP
  tagit: [...]
  ---
  ```
- Väitteet viittaavat lähdesivuun (`[[lahde-...]]`). Ristiriidat merkitään näkyvästi: `> [!warning] Ristiriita: ...`.
- Jokaisella sivulla osio **Katso myös** linkkeineen. Ei orposivuja.

## Työnkulut

### Ingest (uusi lähde)
1. Lue lähde `raw/`-kansiosta (kuvat erikseen tarvittaessa).
2. Keskustele pääkohdista käyttäjän kanssa ennen kirjoittamista (ellei käyttäjä pyydä eräajoa).
3. Luo `wiki/lahteet/lahde-<nimi>.md`.
4. Päivitä / luo käsite- ja työkalusivut; lisää ristiviittaukset molempiin suuntiin; merkitse ristiriidat.
5. Päivitä `yleiskatsaus.md` jos kokonaiskuva muuttuu.
6. Päivitä `index.md`.
7. Lisää merkintä `log.md`:hen.

### Query (kysymys)
1. Lue ensin `index.md`, sitten relevantit sivut.
2. Vastaa viittauksin wikisivuihin.
3. Jos vastaus on arvokas (vertailu, analyysi, uusi yhteys), tarjoudu tallentamaan se `wiki/vastaukset/`-sivuksi ja lisää indeksiin ja lokiin.

### Lint (terveystarkastus)
Etsi: ristiriidat, vanhentuneet väitteet, orposivut, mainitut mutta sivuttomat käsitteet, puuttuvat ristiviittaukset, aukot jotka voisi täyttää verkkohaulla. Raportoi, korjaa sovitusti, kirjaa lokiin.

## Lokin muoto

Jokainen merkintä alkaa: `## [VVVV-KK-PP] <ingest|query|lint|muutos> | <otsikko>`
Viimeiset merkinnät: `grep "^## \[" maarittely/wiki/log.md | tail -5`
