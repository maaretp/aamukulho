---
tyyppi: vastaus
lahteet: [raw/aamiaissovellukset/ominaisuudet.md, raw/aamiaissovellukset/play-kuvaukset/, ../OMINAISUUDET.md, ../README.md]
paivitetty: 2026-11-17
tagit: [aamukulho, kilpailija-analyysi, priorisointi, tuotekehitys]
---

# Aamukulho: miten erottua kilpailijoista (priorisoitu ehdotus)

Kysymys: miten [[aamukulho]] eroaa 12 kilpailijasta ([[aamiaissovellukset]]) ja millä ominaisuuksilla se erottuisi vielä selvemmin?

> [!warning] Varaus
> Kilpailijadata on markkinointitekstiä ([[lahde-aamiaissovellukset-ominaisuudet]]). "Kukaan ei tee X:ää" tarkoittaa, ettei kukaan *mainitse* tekevänsä sitä.

## 1. Vertailu: missä ollaan nyt

| Alue | Aamukulho | Kilpailijat | Tilanne |
|---|---|---|---|
| Hinta per annos, viikkobudjetti, automaattinen halventaminen | ✅ | ❌ kukaan (SID: hinnat vain ostoksissa) | **Ainutlaatuinen** |
| Arki nopea / viikonloppu rauhallinen -automaattitäyttö | ✅ | RIA (käsin) | Harvinainen |
| Koottu valmistelulista (sunnuntai, ~20 min) | ✅ | MOB, RIA mainitsevat ennakkovalmistelun, mutta eivät tehtävälistaa | **Ainutlaatuinen muodoltaan** |
| Ei tiliä, ei mainoksia, data vain laitteella | ✅ | YMP mainokseton; muut vaativat tilin synkronointiin | **Harvinainen** |
| Suomi, suomalaisen marketin ainekset ja hinnat | ✅ | ❌ kaikki englanniksi, USA-kaupat | **Ainutlaatuinen** |
| Piirroskuvat, ei tekoälykuvia | ✅ | ❌ ei mainita | Erottava sävy |
| Kaapista yleensä löytyvät erikseen ostoslistalla | ✅ | PTE (perustuotelista) | Harvinainen |
| Offline | ✅ (https) | END, DIL | Tavallinen |
| Ostoslista osastoittain, rastit | ✅ | lähes kaikki | Perustaso |
| Reseptimäärä | 12 | 1000–240 000 | Tietoinen valinta, ks. kohta 4 |
| Ruokavalio- ja allergiasuodattimet | ❌ | RIA, SAM, SID, JOJ, MPP | **Aukko** |
| Haku raaka-aineella / "mitä kaapissa on" | ❌ | END, MOB, SID, JOJ | Aukko |
| Jaettu ostoslista | ❌ | JOJ, SAM, PTE, YMP, MPP | **Aukko** |
| Omat reseptit käyttöliittymästä | ❌ (vain koodiin) | kaikki | Aukko |
| Kokkaustila (näyttö päällä, ajastin) | ❌ | MOB, REC, SID | Aukko |
| Muistutukset, aamurutiini, kalenteri | ❌ | ❌ **kukaan** | **Vapaa tila** |

**Johtopäätös:** Aamukulhon nykyinen kärki ("halpa, nopea, suomalainen, yksityinen") on jo ainutlaatuinen. Erottuminen kannattaa rakentaa sen päälle eikä kilpailla reseptimäärällä, videoilla tai yhteisöllä.

## 2. Priorisointiperuste

Kukin ehdotus on pisteytetty asteikolla 1–3:
- **E** = erottuvuus (puuttuuko kilpailijoilta?)
- **S** = sopivuus Aamukulhon lupaukseen (alle euro, muutama minuutti, ei tiliä, data laitteella)
- **T** = toteutuksen keveys (yksi HTML-tiedosto, ei palvelinta)

Prioriteetti on pisteiden summa, jota on tarkennettu harkinnalla.

## 3. Ehdotukset priorisoituna

### P1: tee seuraavaksi (vahva erottuvuus ja kevyt toteutus)

**1. Illan valmistelumuistutus ("huomisen aamiainen")** · E3 S3 T2
- Iltanäkymä: "Huomenna tuorepuuro, sekoita kaurat purkkiin nyt (2 min)". Rakennetaan suoraan viikkosuunnitelmasta.
- Kalenteriin: "Lisää kalenteriin" -painike luo `.ics`-tiedoston, jossa on illan valmistelut ja sunnuntain prep-hetki hälytyksineen. Tämä toimii ilman palvelinta ja tiliä, eikä data lähde laitteelta.
- Miksi: tämä on lähteen nimeämä vapaa tila (aamurutiini, kalenteri), jota ei mainitse yksikään 12 sovelluksesta. Se jatkaa luontevasti sunnuntain valmistelulistaa.
- Huom: PWA:n ajastetut push-ilmoitukset vaativat käytännössä palvelimen, joten `.ics` on yksityisyyslupaukseen sopiva ratkaisu.

**2. "Minun tavallinen aamiaiseni" -pikavalinta** · E3 S3 T3
- Merkitse 1–3 vakioaamiaista. "Täytä viikko" käyttää niitä ensisijaisesti ja vaihtelee vain halutessa.
- Vakion kuukausi- ja vuosihinta: "Puurosi maksaa 0,38 €/aamu, 139 €/vuosi".
- Miksi: tämä on lähteen nimeämä aukko. Kilpailijat myyvät vaihtelua ("never cook the same thing twice", MOB), vaikka aamiaisella toisto on normaalia ([[aamiaisen-erityispiirteet]]).

**3. Budjetin näkyvyys vielä pidemmälle: säästölaskuri** · E3 S3 T3
- Vertailu "kahvilan aamupala / valmis smoothie vs. Aamukulho", viikon ja kuukauden säästö.
- Vuosinäkymä: 365 aamua × hinta.
- Miksi: budjetti on Aamukulhon ainoa kiistatta ainutlaatuinen ominaisuus. Se kannattaa tehdä tunteeksi eikä pelkäksi palkiksi.

### P2: tee pian (aukot, jotka estävät käytön, toteutettuna Aamukulhon tavalla)

**4. Ruokavalio- ja allergiasuodattimet: vain olennaiset** · E1 S3 T3
- Gluteeniton, maidoton/laktoositon, kananmunaton, vegaaninen, pähkinätön. Valinta muistetaan, ja "Täytä viikko" sekä budjettivaihto noudattavat sitä.
- Miksi: tämä on perustaso (viidellä kilpailijalla on se). Ilman sitä esimerkiksi keliaakikko perheessä estää koko viikkosuunnitelman käytön. Ei erottava, mutta pakollinen.

**5. Ostoslistan jakaminen ilman tiliä** · E2 S3 T3
- "Jaa lista" Web Share API:lla tekstinä (WhatsApp, viesti) tai linkkinä, jossa lista on koodattuna URL:iin. Ei palvelinta.
- Miksi: jakaminen on aukko (JOJ, SAM, PTE, YMP, MPP), mutta kilpailijoilla se vaatii tilin. Jako ilman tiliä on erottava muoto ja sopii yksityisyyslupaukseen.

**6. Pakkauksen loppujen hyödyntäminen (hävikki × budjetti)** · E3 S3 T2
- Ostoslista kertoo: "Rahkapurkista jää 250 g. Lisää viikolle rahkakulho, niin se ei mene hukkaan". Suunnitelma voi myös itse suosia jo ostettuja pakkauksia.
- Miksi: SID näyttää pakkauksesta käytetyn osuuden, mutta ei kytke sitä suunnitteluun. `ING`-taulukossa on jo yksiköt ja hinnat, joten pakkauskoon lisääminen on kohtuullinen työ.

**7. "Mitä kaapissa on" -pikahaku** · E1 S2 T3
- 12 reseptin kokoelmassa riittää rastilista: "Minulla on kaurat, maito, banaani" → sopivat reseptit ja lisäostojen hinta.
- Miksi: neljällä kilpailijalla on tämä. Aamukulhossa siihen saa mukaan hinnan, mikä tekee siitä tavallista paremman.

### P3: harkitse (erottava, mutta isompi työ tai epävarma hyöty)

**8. Hintojen tuoreus ja kauppavalinta** · E3 S3 T1
- "Hinnat tarkistettu 11/2026". Mahdollinen valinta halpaketju/lähikauppa, jolloin osastojärjestys ja hintataso vaihtuvat.
- Riski: hintojen ylläpito on jatkuvaa käsityötä. Vanhentunut hinta syö budjettilupauksen uskottavuutta. Aloita pelkällä päiväysmerkinnällä.

**9. Omat reseptit käyttöliittymästä, hinta lasketaan automaattisesti** · E2 S2 T1
- Käyttäjä valitsee raaka-aineet `ING`-listasta, ja sovellus laskee hinnan per annos ja proteiinin. Kilpailijoiden reseptintuonnissa ei lasketa hintaa.
- Riski: kasvattaa sovellusta. 12 kuratoidun reseptin selkeys voi kärsiä.

**10. Kevyt aamutila** · E1 S2 T3
- Näyttö pysyy päällä (Wake Lock API), isot vaiheet ja yksi ajastin (puuro, munat). Perustasoa (MOB, REC, SID), mutta halpa tehdä.

**11. "Aamu meni pieleen" -hätänappi** · E2 S3 T3
- Yksi painike, joka näyttää heti kolme 0–3 minuutin vaihtoehtoa siitä, mitä kaapissa yleensä on. Nykyisen vinkkisisällön voi nostaa toiminnoksi.

### Älä tee (kilpailijoiden alue, ei Aamukulhon tapa)
- **Videot, yhteisö, kommentit** (RIA, END, SID, SAM): kalliita ylläpitää, eivätkä sovi yksinkertaisuuslupaukseen.
- **Tekoälysuunnitelmat ja tekoälykuvat** (SAM+, JOJ, YMP): "ilman tekoälykuvia" on jo osa brändiä. Sääntöpohjainen "Täytä viikko" riittää 12 reseptille.
- **Tili ja pilvisynkronointi**: rikkoisi "tietosi pysyvät puhelimessasi" -lupauksen. Jos laitteiden välinen siirto tarvitaan, tee vienti/tuonti tiedostona.
- **Verkkokauppaintegraatio, älylaitteet** (SAM, SID, JOJ): ei suomalaisia rajapintoja, iso työ.
- **Tuhansien reseptien kirjasto**: 12 kuratoitua reseptiä on viesti ("et joudu valitsemaan"), ei puute.

## 4. Ehdotettu positiointi

> **Aamukulho: aamiainen, jota ei tarvitse miettiä.** Sama hyvä aamiainen alle eurolla, valmisteltuna illalla, ilman tiliä.

Kilpailijat lupaavat *vaihtelua ja määrää*. Aamukulho voi luvata *rutiinia, rahaa ja rauhaa*. P1-ominaisuudet (muistutus, vakioaamiainen, säästölaskuri) tukevat juuri tätä viestiä.

## 5. Yhteenveto prioriteeteista

| # | Ominaisuus | E | S | T | Prio |
|---|---|---|---|---|---|
| 1 | Illan valmistelumuistutus + .ics | 3 | 3 | 2 | P1 |
| 2 | Vakioaamiainen-pikavalinta | 3 | 3 | 3 | P1 |
| 3 | Säästölaskuri / vuosihinta | 3 | 3 | 3 | P1 |
| 4 | Ruokavalio-/allergiasuodattimet | 1 | 3 | 3 | P2 |
| 5 | Ostoslistan jako ilman tiliä | 2 | 3 | 3 | P2 |
| 6 | Pakkausten loppujen hyödyntäminen | 3 | 3 | 2 | P2 |
| 7 | "Mitä kaapissa on" + lisäostojen hinta | 1 | 2 | 3 | P2 |
| 8 | Hintojen tuoreus / kauppavalinta | 3 | 3 | 1 | P3 |
| 9 | Omat reseptit hinnalla | 2 | 2 | 1 | P3 |
| 10 | Kevyt aamutila | 1 | 2 | 3 | P3 |
| 11 | "Aamu meni pieleen" -nappi | 2 | 3 | 3 | P3 |

Huom: kohta 4 on pisteiltään matala mutta nostettu P2:een, koska se estää käytön. Kohta 11 on pisteiltään korkea mutta jätetty P3:een, koska vinkkiosio kattaa sen jo osittain.

## Katso myös
[[aamukulho]] · [[aamiaissovellukset]] · [[aamiaisen-erityispiirteet]] · [[lahde-aamiaissovellukset-ominaisuudet]] · [[yleiskatsaus]]
