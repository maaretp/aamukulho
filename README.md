# Aamukulho

Terveelliset arkiaamiaiset, viikon suunnittelu budjetilla, ostoslista ja vinkit. Sovellus on yksi HTML-tiedosto ilman riippuvuuksia.

## Tiedostot

- `index.html` – koko sovellus (reseptit, hinnat ja vinkit ovat tiedoston alussa `ING`- ja `R`-taulukoissa)
- `manifest.webmanifest` – nimi ja kuvake, kun sovellus lisätään kotinäytölle
- `sw.js` – tallentaa sovelluksen puhelimeen, jotta se toimii ilman verkkoa
- `icons/` – sovelluksen kuvakkeet

## Avaaminen omalla koneella

Avaa `index.html` selaimessa tuplaklikkaamalla. Kaikki toimii, paitsi offline-tila.

## Avaaminen puhelimella samasta wifistä

1. Aja tässä kansiossa: `python3 -m http.server 8000`
2. Katso koneen IP-osoite: `ipconfig getifaddr en0`
3. Avaa puhelimen selaimessa `http://<IP-osoite>:8000`
4. Lisää kotinäytölle:
   - iPhone (Safari): Jaa → Lisää Koti-valikkoon
   - Android (Chrome): ⋮ → Lisää aloitusnäytölle

Offline-tila vaatii https-osoitteen. Sen saa, kun sovellus julkaistaan esimerkiksi GitHub Pagesiin tai Netlifyyn.

## Tallennus

Viikkosuunnitelma, budjetti, ostoslistan ruksit ja omat kuvat tallentuvat vain kyseisen laitteen selaimeen (`localStorage`). Ne eivät siirry laitteelta toiselle.

## Reseptin lisääminen

Lisää `R`-taulukkoon uusi rivi samassa muodossa kuin muut. Jos reseptissä on uusi raaka-aine, lisää se myös `ING`-taulukkoon yksikön, yksikköhinnan ja kaupan osaston kanssa. Hinta per annos lasketaan automaattisesti.
