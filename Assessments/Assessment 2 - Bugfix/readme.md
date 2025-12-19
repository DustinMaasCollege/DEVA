# Sollicitatie-opdracht 2 – Bugfixing & Debugging

## Algemene voorwaarden

Tijdens deze opdracht werk je zoals je dat ook in een professionele werkomgeving zou doen. Je mag en wordt zelfs aangemoedigd om moderne hulpmiddelen en methodieken te gebruiken, zoals online documentatie, Stack Overflow en AI-tools (bijvoorbeeld ChatGPT, Claude, Cursor of vergelijkbaar).

### Belangrijke uitgangspunten

* Je werkt consequent volgens één duidelijke methodiek (bijvoorbeeld MVC, service layer, policies, middleware)
* Je licht toe welke beveiligingsprincipes of -structuur je hanteert
* Je gebruikt GitHub voor versiebeheer
* Je toont initiatief en creativiteit; er is ruimte voor eigen keuzes en ideeën
* Alle opdrachten zijn gebaseerd op Laravel (backend) en Tailwind CSS (frontend)
* De opdracht is zo opgezet dat deze binnen maximaal 4 uur afgerond kan worden

---

## De verwachting

### 1. Korte toelichting

Beschrijf:
* Hoe je de opdracht lokaal werkend hebt gekregen
* Welke tools en hulpmiddelen je hebt gebruikt
* Welke keuzes je bewust hebt gemaakt (en waarom)

### 2. Resultaat

Voor deze opdracht lever je werkende code aan waarin de fout is opgelost.
De focus ligt **niet** op "perfectie", maar op denkproces, aanpak en professionaliteit.

---

## De opdracht

In deze map vind je een [archief](./opdracht_2_bugfixing.zip) met een Laravel-installatie waarin een concrete foutmelding optreedt (bijvoorbeeld een exception, verkeerde data, of logische fout).

De opdracht is om:
* De fout te analyseren
* Deze op te lossen
* Inzichtelijk te maken hoe je tot de oplossing bent gekomen

### Richtlijnen

* Laat zien hoe je debugt:
   * Logs
   * Dumps (dd(), dump(), Ray, etc.)
   * Debugging tools (Xdebug, Telescope, browser DevTools)
* De oplossing hoeft niet "mooier dan nodig" te zijn, zolang deze correct en uitlegbaar is
* Documenteer je proces: welke stappen heb je doorlopen?

### Verwachte uitkomst

* Een werkende applicatie
* Korte beschrijving (in [Prompts and Descriptions](./prompts%20and%20descriptions.md) of boven de aangepaste code):
   * Wat was de fout?
   * Wat was de oorzaak?
   * Hoe heb je deze opgelost?
   * Welke debugging-technieken heb je toegepast?
* Git commits waarin het probleem en de oplossing herkenbaar zijn
   * Bijvoorbeeld: "fix: resolve N+1 query issue in UserController"
   * Of aparte commits per stap als je meerdere issues tegenkwam

### Extra aandachtspunten

* Heb je geautomatiseerde tests toegevoegd om herhaling te voorkomen?
* Heb je de onderliggende oorzaak aangepakt of alleen het symptoom?
* Zijn er bredere verbeteringen die je zou aanraden?

### Voorbeelden van mogelijke bugs

1. **Performance issue**: Een pagina laadt extreem traag door N+1 queries
2. **Logic error**: Een berekening geeft verkeerde resultaten door type coercion
3. **Exception**: Een undefined index/property error in een specifiek scenario
4. **Frontend issue**: JavaScript werkt niet door Tailwind/Alpine.js conflicten
5. **Validation bug**: Formulieren accepteren ongeldige data

Gebruik de Laravel installatie in het meegeleverde [archief](./opdracht_2_bugfixing.zip) om de bug op te lossen.

---

## Inleveren

* GitHub repository link (public of toegang voor ons account)
* prompts and descriptions.md met je proces-beschrijving
* Werkende Laravel applicatie
* Duidelijke commit history

Succes!
