# PayPal Checkout Testproject

Een eenvoudig testproject om PayPal betaalintegratie te demonstreren en te evalueren.

## Projectbeschrijving

Dit project is opgezet om de PayPal betaalintegratie te testen en te demonstreren hoe je PayPal kunt implementeren in een webapplicatie. Het bevat:

1. Een basisproduct met PayPal betaalknop
2. Een pagina met verschillende PayPal knopstijlen om te vergelijken
3. Eenvoudige documentatie over beschikbare opties

## Vereisten

- Node.js moet op je computer geïnstalleerd zijn

## Installatie

1. Download of clone dit project naar je computer
2. Open een terminal of command prompt
3. Navigeer naar de projectmap
4. Installeer de benodigde dependencies:

```bash
npm install
```

5. Start de server:

```bash
npm start
```

6. Open je browser en ga naar: http://localhost:3000

## Hoe het werkt

### Technische details
- De frontend is gemaakt met HTML, CSS en JavaScript
- Er is een eenvoudige Node.js server (met Express) om de statische bestanden te serveren
- De PayPal integratie maakt gebruik van de PayPal JavaScript SDK
- Voor demonstratiedoeleinden gebruiken we de PayPal sandbox omgeving

### PayPal Integratie
De integratie bestaat uit drie hoofdstappen:
1. **PayPal SDK laden** - Via een script tag met client-ID
2. **Bestelling aanmaken** - Via de `createOrder` functie
3. **Betaling verwerken** - Via de `onApprove` functie

### Projectstructuur
- `index.html` - Hoofdpagina met PayPal betaalknop
- `button-styles.html` - Pagina met verschillende PayPal knopstijlen
- `styles.css` - CSS-stijlen voor het project
- `server.js` - Express server om de applicatie te draaien
- `package.json` - Projectdependencies
- `PayPal-Button-Options.md` - Documentatie over PayPal knopopties

## Testen van de PayPal Integratie

- Als je op de PayPal-knop klikt, word je naar de PayPal sandbox-omgeving geleid
- Voor testdoeleinden kun je de volgende PayPal sandbox-inloggegevens gebruiken:
  - E-mail: sb-47bfqf29049300@personal.example.com
  - Wachtwoord: 12345678

## PayPal Knopstijlen

Dit project bevat een pagina om verschillende PayPal knopstijlen te vergelijken:
- Ga naar http://localhost:3000/button-styles.html
- Deze pagina toont verschillende layouts en kleuren zodat je kunt kiezen welke het beste bij je website past
- Bekijk `PayPal-Button-Options.md` voor meer gedetailleerde informatie over knopstijlingsopties

## Voor productiegebruik

Dit is een testproject met de sandbox-omgeving van PayPal. Voor een productieomgeving moet je:
1. De 'test' client-ID vervangen door je eigen PayPal client-ID
2. Server-side code implementeren voor het verwerken van bestellingen en betalingen
3. Foutafhandeling en transactielogging toevoegen
4. Een veilige HTTPS-verbinding gebruiken

## Aanpassingen en uitbreidingen

Je kunt dit project gebruiken als basis en aanpassen naar jouw behoeften:
- Voeg meerdere producten toe
- Implementeer een winkelwagen
- Voeg andere betaalmethoden toe om te vergelijken
- Bouw een dashboard voor betalingsinformatie

---

Dit project is gemaakt als testproject om PayPal-integratie te evalueren en te vergelijken met andere betaalmethoden. 
