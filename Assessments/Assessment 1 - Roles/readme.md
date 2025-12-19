# Sollicitatie-opdracht 1 – Rollen & Rechten (architectuur en aanpak)

## Algemene voorwaarden

Tijdens deze opdracht werk je zoals je dat ook in een professionele werkomgeving zou doen. Je mag en wordt zelfs aangemoedigd om moderne hulpmiddelen en methodieken te gebruiken, zoals online documentatie, Stack Overflow en AI-tools (bijvoorbeeld ChatGPT, Claude, Cursor of vergelijkbaar).

### Belangrijke uitgangspunten

* Je werkt consequent volgens één duidelijke methodiek (bijvoorbeeld MVC, service layer, policies, middleware)
* Je licht toe welke beveiligingsprincipes of -structuur je hanteert
* Je gebruikt GitHub (of GitHub-compatible) voor versiebeheer
* Je toont initiatief en creativiteit; er is ruimte voor eigen keuzes en ideeën
* Alle opdrachten zijn gebaseerd op Laravel (backend) en Tailwind CSS (frontend)
* De opdracht is zo opgezet dat deze binnen maximaal 4 uur afgerond kan worden

---

## De verwachting

### 1. Korte toelichting (max. ±½ A4)

Beschrijf:
* Hoe je de opdracht lokaal werkend hebt gekregen
* Welke tools en hulpmiddelen je hebt gebruikt
* Welke keuzes je bewust hebt gemaakt (en waarom)

### 2. Resultaat

Voor deze opdracht lever je een technische opzet aan die laat zien hoe je tegen het probleem aankijkt.
De focus ligt **niet** op "perfectie", maar op denkproces, aanpak en professionaliteit.

---

## De opdracht

Ontwerp een eerste opzet voor een rollen- en rechtenstructuur binnen een Laravel-applicatie.

Het hoeft nog niet volledig functioneel te zijn; we willen vooral zien hoe je dit zou aanvliegen en hoe je structuur aanbrengt.

### Richtlijnen

* Denk na over:
   * Migrations / seeds (optioneel)
   * Middleware, services, policies of controllers
* We willen minimaal één centrale functie of methode zien die bepaalt of een pagina wel of niet getoond mag worden op basis van een rol
* De nadruk ligt op pagina-toegang, niet op losse acties
* Je mag zelf kiezen of je migrations/seeds gebruikt; beide zijn toegestaan maar niet noodzakelijk voor het slagen van de opdracht
* De rollen zijn (op volgorde): 1. Administrator, 2. Directeur, 3. Manager, 4. Teamleider en 5. Teamlid

### Verwachte uitkomst

* Minimaal één van de volgende methodes gebruikt:
   * Controller
   * Middleware
   * Service
* Inclusief:
   * Duidelijke naamgeving
   * Korte toelichting (commentaar of README) over je keuzes
* Eventueel een eenvoudige route of view ter illustratie

### Extra aandachtspunten

* Hoe schaalbaar is jouw oplossing?
* Hoe zou je dit uitbreiden naar meer granulaire rechten (bijvoorbeeld acties in plaats van alleen pagina's)?
* Welke Laravel-conventies hanteer je?

---

## Inleveren

* GitHub repository link (public of toegang voor ons account)
* README.md met je toelichting
* Code in een werkende Laravel-structuur (minimaal de relevante bestanden)

Succes!
