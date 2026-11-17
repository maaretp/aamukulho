---
name: kielletyt-ruokayhdistelmat
description: Tarkistaa, ettei resepteissä, ruokalistoissa, ateriasuunnitelmissa, ostoslistoissa tai ruokaehdotuksissa yhdistetä kiellettyjä ruoka-aineita (esim. maapähkinävoi + hillo, makkara + hillo). Käytä aina kun ehdotat, kirjoitat, muokkaat tai arvioit ruokaa, reseptiä, voileipää, välipalaa, eväitä tai ateriaa – myös kun käyttäjä vain pyytää ideoita.
---

# Kielletyt ruokayhdistelmät

Tämä skill varmistaa, ettei samaan ruokaan, annokseen tai ateriaan yhdistetä ruoka-aineita, jotka on merkitty kielletyiksi pareiksi.

## Kielletyt yhdistelmät

| Ruoka-aine A | Ruoka-aine B | Huom. |
|---|---|---|
| maapähkinävoi | hillo | myös marmeladi, hyytelö, "PB&J" |
| makkara | hillo | kaikki makkarat (nakki, grillimakkara, lenkki, salami, chorizo…) ja kaikki hillot |

Lisää uudet kielletyt parit tähän taulukkoon.

## Mitä lasketaan samaksi ruoka-aineeksi

Tulkitse ruoka-aineet laajasti – tarkoitus on estää yhdistelmä, ei vain tarkkaa sanaa:

- **hillo**: hillo, marmeladi, hyytelö, sose, kiisseli-tyyppiset marjalevitteet, puolukkahillo, jelly, jam, preserves, chutney jos se on makea hedelmälevite.
- **maapähkinävoi**: maapähkinävoi, maapähkinälevite, peanut butter, maapähkinäkastike (satay) jos se toimii levitteenä tai kastikkeena samassa annoksessa.
- **makkara**: kaikki makkarat ja nakit, myös leikkeleenä (salami, meetvursti), kasvisnakit ja -makkarat.

Jos olet epävarma kuuluuko aines kiellettyyn ryhmään, oleta että kuuluu ja mainitse asia käyttäjälle.

## Mikä lasketaan yhdistelmäksi

Yhdistelmä on kielletty, kun molemmat ainekset ovat:

- samassa reseptissä tai ainesosaluettelossa,
- samassa annoksessa, voileivässä, välipalassa tai eväsrasiassa,
- samalla lautasella tarjoiluehdotuksena (esim. "makkaran kanssa puolukkahilloa"),
- tarjoiluehdotuksena tai "sopii hyvin yhteen" -suosituksena.

Eri päivien tai eri aterioiden ruokalistalla ne saavat esiintyä erikseen.

## Toimintaohje

1. **Ennen vastausta** käy läpi kaikki ehdottamasi tai käyttäjän antamat ruoka-aineet ja vertaa niitä yllä olevaan taulukkoon.
2. **Jos itse olisit ehdottamassa kiellettyä yhdistelmää**, vaihda toinen aines sopivaan korvikkeeseen, esim.:
   - maapähkinävoi + hillo → maapähkinävoi + banaani, tai juusto + hillo
   - makkara + hillo → makkara + sinappi, tai makkara + perunamuusi ja kurkku
3. **Jos käyttäjä pyytää kiellettyä yhdistelmää** tai sitä on hänen antamassaan reseptissä:
   - kerro selvästi, mikä pari on kielletty ja missä kohtaa se esiintyy,
   - ehdota 1–2 vaihtoehtoa,
   - älä toteuta yhdistelmää ellei käyttäjä erikseen vahvista, että haluaa poiketa säännöstä.
4. **Tarkistuksen tulos**: kun arvioit reseptiä tai listaa, ilmoita lyhyesti joko
   - `✅ Ei kiellettyjä yhdistelmiä`, tai
   - `⚠️ Kielletty yhdistelmä: <A> + <B> (<missä>)` ja korjausehdotus.

## Esimerkkejä

- "Tee eväsleipä lapselle" → ✅ ehdota esim. maapähkinävoi + banaani, **ei** maapähkinävoi + hillo.
- "Grilli-illan menu: grillimakkaraa, puolukkahilloa, perunasalaattia" → ⚠️ makkara + hillo samalla aterialla; ehdota sinappia tai ketsuppia hillon tilalle.
- "Maanantaina lettuja ja hilloa, tiistaina makkarakeittoa" → ✅ eri aterioilla, sallittu.
