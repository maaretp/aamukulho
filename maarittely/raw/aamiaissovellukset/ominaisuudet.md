# Aamiaissovelluksen ominaisuudet – verkkohaun kooste

- **Haettu:** 2026-11-17, playwright-cli
- **Menetelmä:** Google Play -haku "breakfast recipes planner" → 12 sovelluksen kuvaukset (alkuperäiset tekstit: `play-kuvaukset/`). DuckDuckGo vaati CAPTCHAn ja Bing palautti aiheeseen liittymättömiä tuloksia, joten hakukoneita ei käytetty.
- **Rajaus:** Lähteinä ovat sovelluskauppojen markkinointikuvaukset, eivät käyttäjäarviot tai testaus. Väitteet kuvaavat, mitä sovellukset *sanovat* tekevänsä.

## Tarkastellut sovellukset

| Lyhenne | Sovellus | Tyyppi | Tähdet* |
|---|---|---|---|
| RIA | Breakfast Recipes & Planner (Riafy) | aamiaisreseptit + suunnittelu | 3.5 |
| END | Breakfast Recipes Cookbook App (Firehawk) | aamiaisreseptit | 4.7 |
| EDU | Healthy Breakfast Recipes Book (Edutainment Ventures) | aamiaisreseptit | 4.x |
| DIL | Breakfast Recipes (DIL Studio) | aamiaisreseptit, offline | 4.8 |
| SAM | Samsung Food: Meal Planner | yleinen ateriasuunnittelu | 4.4 |
| REC | ReciMe: Recipes & Meal Planner | reseptien keräys + suunnittelu | 4.6 |
| SID | SideChef: Recipes & Meal Plans | reseptit + ostokset + älylaitteet | 4.5 |
| PTE | Plan to Eat: Meal Planner | suunnittelu, maksullinen | 4.7 |
| JOJ | Meal Planner & Grocery List (JoJo Apps) | suunnittelu + ruokakomero | 4.7 |
| MOB | Mob: Meal Planner and Recipes | reseptit + suunnittelu | 4.3 |
| MPP | Meal Prep: Planner & Recipes (Wideapp) | suunnittelu | 4.6 |
| YMP | Meal Planner & Macro Tracker (YouMealPlan) | suunnittelu + ravinto | 4.7 |

\* Google Playn hakutuloksessa näkynyt arvio hakuhetkellä.

## Ominaisuudet kategorioittain

### 1. Reseptit ja sisältö
- Laaja aamiaisreseptikirjasto: pannukakut, munakkaat, smoothiet, puurot, muffinssit, vuoat (RIA, END, EDU, DIL)
- Vaiheittaiset ohjeet; kuva tai video jokaisessa vaiheessa (END, SID, RIA, DIL)
- Videoreseptit ja tekniikkavideot, esim. munien vatkaus, pannukakun kääntö (RIA, END, SID)
- Kategoriat ja kokoelmat: arkiaamut, viikonlopun brunssi, juhlapyhät (pääsiäinen) (RIA, DIL, SID)
- Nopeat vaihtoehdot: "5 minuutin mukaan otettava", useimmat alle 30 min (RIA, DIL)
- Aloittelijaystävälliset ja lapsille sopivat reseptit (RIA, SID, MOB)
- Uusia reseptejä viikoittain omilta kokeilta (MOB)
- Juomat: kahvi, tuoremehu, smoothiet, pirtelöt (EDU)

### 2. Haku ja suodatus
- Haku nimellä tai raaka-aineella (DIL, EDU, MPP, SAM, PTE)
- "Mitä jääkaapissa on" -haku: syötä esim. 5 raaka-ainetta → reseptit (END, MOB, SID, JOJ)
- Ruokavaliosuodattimet: gluteeniton, vegaani, kasvis, pescetaristi, low-carb, keto, paleo, FODMAP, pätkäpaasto ym. (RIA, SAM, SID, JOJ, MPP)
- Allergeenisuodattimet: gluteeni, kananmuna, maito, soija, maapähkinä, pähkinät, kala, äyriäiset (SID, JOJ)
- Poissulkeva suodatin: "en halua nähdä tätä" / vältettävät raaka-aineet (EDU, MPP, JOJ)
- Suodatus valmistusajan, maun (makea, suolainen, tulinen), valmistustavan (paisto, keitto, uuni) ja keittiön mukaan (EDU, SAM, MPP)
- Suodatus käytettävissä olevien keittiövälineiden mukaan (MPP)

### 3. Ateriasuunnittelu
- Viikon aamiaissuunnitelma etukäteen; arkiaamuille nopeat, viikonlopuille isommat (RIA)
- Kalenterinäkymä; päivä, viikko, kuukausi tai vapaa aikaväli (MPP, JOJ)
- Aterioiden vaihto ja siirto vedä ja pudota -toiminnolla (MPP, JOJ, PTE)
- Toistuvuuden säätö: kuinka usein sama ateria toistuu (MPP)
- Automaattinen tai tekoälyllä tuotettu suunnitelma ruokavalion, allergioiden, inhokkien ja henkilömäärän mukaan (SAM+, JOJ)
- Suunnitelmapohjat ja aiempien viikkojen uudelleenkäyttö (SAM+, YMP)
- Tähteiden ja pakastettujen aterioiden suunnittelu (PTE)
- Ennakkovalmistelu / meal prep, edellisenä iltana tehtävät aamiaiset ("preppable breakfasts") (MOB, RIA)
- Tulostettava ruokalista (JOJ)

### 4. Ostoslista ja ostokset
- Ostoslista luodaan automaattisesti suunnitelmasta tai reseptistä yhdellä napautuksella (lähes kaikki)
- Lista ryhmiteltynä kaupan hyllyjen tai reseptin mukaan; samat raaka-aineet yhdistetään (MOB, REC, MPP)
- Omat lisäkohteet, perustuotteiden (staples) lista, kauppakohtaiset listat (PTE)
- Rasti ruutuun ostettaessa (MPP, YMP)
- Viivakoodinlukija (JOJ)
- Verkkokauppaintegraatio: tilaus suoraan kotiin, esim. Instacart, Walmart, Amazon Fresh (SAM, REC, SID, JOJ)
- Reaaliaikaiset hinnat ja saatavuus; kuinka suuri osa pakkauksesta kuluu → hävikin vähentäminen (SID)

### 5. Ruokakomero ja hävikki
- Ruokakomeron/jääkaapin seuranta; suunnitelma rakennetaan olemassa olevista raaka-aineista (JOJ, SAM+)
- Pilaantuvien käyttö ennen kuin ne menevät huonoiksi (JOJ)
- Annoskoon skaalaus, jotta ostetaan vain tarvittava (MOB, REC, PTE, MPP)

### 6. Ravinto ja terveys
- Ravintoarvot jokaiselle reseptille ja raaka-aineelle (EDU, SAM, MOB, RIA)
- Kalorit ja makrot (proteiini, hiilihydraatit, rasva, sokeri, kuitu) (REC, YMP, MOB)
- Päivittäiset ravintotavoitteet ja seuranta; aloitusnäytön widget (YMP)
- Ravintoarvion pyytäminen tekoälyltä vapaamuotoisen kuvauksen perusteella; huomautus "ei lääketieteellinen neuvo" (YMP)
- Terveyspisteet (health score) (SAM)
- Proteiinipitoiset ja kevyet vaihtoehdot (MOB, RIA)

### 7. Reseptien tuonti ja oma reseptikirja
- Tuonti URL:sta tai jaa-valikosta (PTE, JOJ, SAM, YMP)
- Tuonti sosiaalisesta mediasta: Instagram, TikTok, YouTube, Pinterest, Facebook (REC, YMP)
- Kuvasta tai käsin kirjoitetusta reseptikortista tekoälyllä ("mummon reseptit") (JOJ, REC)
- Tuonti muista sovelluksista: Paprika, Notion, Evernote, Google Docs (REC)
- Omat reseptit käsin; kokoelmat ja keittokirjat; suosikit ja kirjanmerkit (kaikki)
- Haku omasta reseptikirjasta otsikon, tagien, arvion ym. mukaan (PTE)

### 8. Kokkaustila
- Näyttö pysyy päällä kokatessa (MOB, REC)
- Handsfree / ääniohjeet: sovellus lukee ohjeet ääneen (EDU, SAM+)
- Sisäänrakennetut ajastimet (SID)
- Mittayksiköiden muunnos metrinen ↔ US (REC, MPP)
- Reseptin muokkaus: annokset, raaka-aineet, ravinto (SAM+)

### 9. Jakaminen ja yhteisö
- Jaettu ostoslista ja suunnitelma perheen tai kumppanin kanssa reaaliajassa (JOJ, SAM, PTE, YMP, MPP)
- Reseptin jako tekstiviestillä, sähköpostilla, WhatsAppilla, AirDropilla (REC, PTE)
- Omien reseptien ja kuvien julkaisu yhteisölle (END, EDU, SID)
- Arviot, kommentit, vinkit, epäonnistumisten jakaminen (SID, SAM)
- Ruokayhteisöt/ryhmät (SAM)

### 10. Alusta ja käytettävyys
- Toimii offline (END, DIL)
- Synkronointi laitteiden välillä: puhelin, tablet, verkko (PTE, REC, YMP)
- Widgetit: suunnitelma, ostoslista tai ravinto näkyy avaamatta sovellusta (JOJ, YMP)
- Yksinkertainen navigointi, kuvat reseptilistassa (END, DIL)
- Mainokseton ydinkäyttö (YMP)

### 11. Älykeittiö
- Älylaitteiden etäohjaus resepteistä: LG, GE, Bosch Home Connect (SID)
- Samsung SmartThings Cooking -integraatio (SAM+)

### 12. Ansaintamallit (havainto)
- Ilmainen + premium-tilaus (SAM+, REC, SID, MOB, YMP); premiumissa tyypillisesti tekoälysuunnitelmat, rajaton tuonti, ravintolaskenta
- Pelkkä maksullinen tilaus kokeilujakson jälkeen (PTE: 14 pv, $5.95/kk tai $49/v)
- Tilaushinnat: SID $4.99/kk tai $49.99/v

## Havaintoja aamiaissovelluksen näkökulmasta

- **Puhtaat aamiaissovellukset** (RIA, END, EDU, DIL) ovat lähinnä reseptikirjoja. Niiden kärki on videot, offline-käyttö ja aamiaiskategoriat. Suunnittelu ja ostoslista ovat kevyitä.
- **Yleiset ateriasuunnittelijat** (SAM, REC, SID, PTE, JOJ, MOB, MPP, YMP) ovat monipuolisempia, mutta aamiainen on niissä vain yksi aterian tyyppi.
- **Aamiaiselle ominaista** lähteissä: aamukiire ("5 min grab-and-go"), arki- ja viikonloppuaamujen ero, edellisenä iltana valmisteltavat aamiaiset, brunssi juhlapyhinä, juomat ja lasten suosikit.
- **Ei löytynyt yhdestäkään lähteestä:** aamurutiiniin sidottu ajoitus tai muistutukset (esim. "laita kaurat likoamaan illalla"), herätykseen tai kalenteriin kytkeytyminen, toistuvan "tavallisen aamiaisen" pikavalinta. Nämä ovat mahdollisia eroavuuksia, mutta niiden puuttuminen perustuu vain näihin 12 kuvaukseen.
