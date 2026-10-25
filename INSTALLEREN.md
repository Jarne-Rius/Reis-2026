# Reisplanner – installeren (eenmalig)

## 1. Online zetten met GitHub Pages (gratis)
1. Maak op github.com een account en een nieuwe **publieke** repository, bv. `reisplanner`.
2. Kies "Add file → Upload files" en sleep alle bestanden uit deze map erin (index.html, sw.js, manifest.webmanifest en de drie png-iconen). Commit.
3. Ga naar Settings → Pages → Source: "Deploy from a branch", branch `main`, map `/ (root)`. Na ± 1 minuut staat de app op `https://JOUWNAAM.github.io/reisplanner/`.
   De code bevat geen persoonlijke gegevens: je planning en documenten staan alleen in je eigen Google Drive en op je toestellen.

## 2. Google Client-ID aanmaken (5 min, op een computer)
1. console.cloud.google.com → nieuw project.
2. "API's en services" → Bibliotheek → **Google Drive API** inschakelen.
3. OAuth-toestemmingsscherm: type Extern, naam + je e-mailadres, voeg je Google-account toe als testgebruiker, en zet daarna op "In productie" (anders verloopt de toestemming na 7 dagen). De gebruikte rechten (verborgen app-map in Drive) zijn niet gevoelig.
4. Inloggegevens → Inloggegevens maken → OAuth-client-ID → **Webtoepassing**.
   - Geautoriseerde JavaScript-bronnen: `https://JOUWNAAM.github.io`
   - Geautoriseerde omleidings-URI: `https://JOUWNAAM.github.io/reisplanner/`
5. Kopieer de Client-ID.

## 3. Op de iPhone
1. Open de link in **Safari** → tab ⚙ → plak de Client-ID → Bewaar → "Aanmelden met Google".
2. Tik op "Startbestand importeren" en kies `reisplanner-startbestand.json` (dat bestand krijg je apart, zet het niet op GitHub). Alles gaat naar je Drive.
3. Deel-knop → "Zet op beginscherm". Laat "Open als webapp" uit.
4. Op de iPhone van je vriendin: dezelfde link, dezelfde Client-ID, aanmelden met hetzelfde Google-account. De planning komt vanzelf binnen.

Zonder internet blijft alles werken, inclusief de documenten die één keer met internet zijn geopend of gesynchroniseerd. Wijzigingen gaan naar Drive zodra er weer verbinding is.
