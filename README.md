# Lyra WMS Nieuwsbrief Builder

Een webformulier waarmee je de maandelijkse nieuwsbrief van Lyra WMS invult en direct de HTML krijgt voor het HTML-blok in HubSpot. Geen technische kennis nodig.

## Zo gebruik je het

1. Open de builder in je browser.
2. Vul de velden in. Rechts zie je meteen een preview (desktop en mobiel).
3. Kijk bij **Check** of er nog iets ontbreekt, zoals een link of een afbeelding die niet in HubSpot staat.
4. Klik op **Kopieer HTML** en plak het in het HTML-blok van je HubSpot-marketingmail.

Wat je invult blijft bewaard in je browser. Met **Concept opslaan** download je je invoer als bestand, zodat een collega het met **Concept laden** kan openen en afmaken.

## Regels die de builder automatisch toepast

- Logo, hero en afsluiting staan er altijd in.
- Optionele secties (Nieuwe functies, Nieuws, Tip, Kaarten) verschijnen alleen als je ze invult.
- Afbeeldingen alleen als er een URL is. Upload ze in HubSpot Bestanden, 1040 px breed.
- Eén kaart wordt over de volle breedte getoond, twee kaarten naast elkaar.
- Doelgroep **Prospects**: lege knop wordt automatisch "Plan een gesprek" met de Calendly-link.
- Doelgroep **Klanten**: knoptekst en link vul je zelf in.
- Bijzondere tekens (é, ë, &, emoji) worden automatisch omgezet naar HTML-entiteiten.
- Ontbrekende links worden `#` en verschijnen in de check.

## Online zetten via GitHub Pages

1. Maak op GitHub een nieuwe repository aan, bijvoorbeeld `lyra-nieuwsbrief-builder`.
2. Upload `index.html` en `README.md` via **Add file → Upload files** en klik op **Commit changes**.
3. Ga naar **Settings → Pages**.
4. Kies bij **Source** voor **Deploy from a branch**, selecteer `main` en map `/ (root)`, en klik op **Save**.
5. Na een minuut staat de builder online op `https://<jouw-gebruikersnaam>.github.io/lyra-nieuwsbrief-builder/`. Deel die link met je collega's.

Let op: GitHub Pages is gratis voor openbare repositories. Bij een privé repository heb je een betaald GitHub-abonnement nodig. In de builder staan geen geheime gegevens, alleen de template, het logo en de Calendly-link.

## Aanpassen

Vaste gegevens staan bovenaan het script in `index.html`:

```js
const LOGO_URL = '...';
const CALENDLY = 'https://calendly.com/thies-lyrawms/30min';
const AFZENDER = 'Thies';
```

Wil een collega onder eigen naam versturen, pas dan `AFZENDER` aan. Wijzigingen aan de opmaak van de mail zelf doe je in de functie `generate()`.

## Onderwerpregel en preview-tekst

Die maakt de builder niet. Vul ze zelf in HubSpot in, of laat Claude in het project "Lyra WMS nieuwsbrief" een paar opties maken.
