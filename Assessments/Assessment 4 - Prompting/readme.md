# Sollicitatie-opdracht 4 – How to Prompt: AI-Assisted Development

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

### 1. Korte toelichting

Beschrijf:
* Hoe je de opdracht hebt aangepakt
* Welke AI-tools je hebt gebruikt en waarom
* Welke prompting-strategieën je hebt toegepast
* Welke keuzes je bewust hebt gemaakt (en waarom)

### 2. Resultaat

Voor deze opdracht lever je een kritische analyse aan van AI-gegenereerde code, inclusief je eigen verbeteringen.

De focus ligt niet op "perfectie", maar op denkproces, aanpak en professionaliteit.

---

## De opdracht

In de moderne softwareontwikkeling is AI een steeds belangrijker hulpmiddel. Maar AI is geen vervanging voor jouw expertise – het is een tool die je slim moet kunnen inzetten en waarvan je de output kritisch moet kunnen beoordelen.

In deze opdracht laat je zien:
1. **Hoe je effectief communiceert met AI-tools** (prompting)
2. **Hoe je gegenereerde code beoordeelt** (code review skills)
3. **Hoe je AI-output verbetert tot productieklare code** (refactoring)

### Fase 1: AI-Assisted Development (±2 uur)

Gebruik een AI-tool naar keuze (ChatGPT, Claude, Cursor, GitHub Copilot, etc.) om een van onderstaande features te laten genereren:

**Optie A: Authentication met 2FA**
Implementeer een two-factor authentication systeem in Laravel (via email of authenticator app)

**Optie B: File Upload met Processing**
Bouw een systeem voor het uploaden en verwerken van bestanden (bijvoorbeeld: afbeeldingen resizen, PDFs indexeren, CSV importeren)

**Optie C: Geavanceerde Zoekfunctie**
Implementeer een zoekfunctie met filters, sorting, en pagination (bijvoorbeeld: product catalogus, artikel database)

#### Wat je moet doen:

1. **Documenteer je prompts**: Bewaar alle prompts die je gebruikt hebt
2. **Iteratief werken**: Laat zien hoe je de AI stuurt naar betere output
3. **Code genereren**: Laat de AI zo veel mogelijk code voor je schrijven
4. **Code review**: Laat met commits zien hoe je de AI code hebt gecorrigeerd/gecontroleerd

### Fase 2: Code Assessment (±1,5 uur)

Beoordeel de gegenereerde code kritisch op:

1. **Functionaliteit**
   * Werkt de code zoals bedoeld?
   * Zijn er edge cases die niet worden afgehandeld?
   
2. **Code kwaliteit**
   * Volgt de code Laravel best practices?
   * Is de code leesbaar en maintainable?
   * Is er sprake van code duplication?
   
3. **Security**
   * Zijn er security vulnerabilities? (SQL injection, XSS, CSRF, etc.)
   * Wordt input correct gevalideerd?
   * Zijn er authorization checks?
   
4. **Performance**
   * Zijn er N+1 query problemen?
   * Wordt caching goed toegepast?
   * Is de code efficient?
   
5. **Testing**
   * Is de code testbaar?
   * Ontbreken er belangrijke tests?

### Fase 3: Refactoring & Verbetering (±30 min)

Verbeter de gegenereerde code op basis van je assessment. Leg uit:
* Wat je hebt aangepast en waarom
* Welke patterns of best practices je hebt toegepast
* Waar de AI het goed deed en waar het tekortschoot

### Verwachte uitkomst

Lever in:

1. **Prompt log** (Markdown bestand)
   * Alle prompts die je hebt gebruikt
   * Per prompt: wat was je doel? Wat was het resultaat?
   * Reflectie: welke prompting technieken werkten goed?

2. **Code Assessment rapport** (Markdown of PDF)
   * Gestructureerde beoordeling per categorie (zie Fase 2)
   * Concrete voorbeelden van problemen met code snippets
   * Overzicht van gevonden issues met severity (critical/major/minor)

3. **Refactored code** (GitHub repository)
   * Originele AI-gegenereerde code (in aparte branch: `ai-generated`)
   * Jouw verbeterde versie (in `main` branch)
   * Clear commit messages die je refactoring stappen tonen

4. **README.md** met:
   * Welke AI tool(s) je hebt gebruikt
   * Samenvatting van belangrijkste bevindingen
   * Je algemene conclusie over AI-assisted development
   * Best practices die je hieruit hebt geleerd

### Beoordelingscriteria

We kijken naar:

* **Prompting skills**: Kun je effectief communiceren met AI?
* **Code review skills**: Kun je code kritisch beoordelen?
* **Technical knowledge**: Herken je security issues, performance problemen, en best practice violations?
* **Problem solving**: Kun je problemen oplossen en code verbeteren?
* **Professional approach**: Documenteer je je werk goed?

### Tips voor succesvol AI-gebruik

**Goede prompting technieken:**
* Wees specifiek over context (Laravel versie, packages, requirements)
* Vraag om toelichting bij gegenereerde code
* Vraag om alternatieven en trade-offs
* Geef feedback op de output en vraag om verbeteringen
* Splits complexe problemen op in kleinere delen

**Rode vlaggen in AI-gegenereerde code:**
* Ontbrekende validation
* Hardcoded credentials of secrets
* Geen error handling
* Inefficiënte queries
* Verouderde syntax of deprecated methods
* Ontbrekende authorization checks
* Over-engineered oplossingen voor simpele problemen

---

## Inleveren

* GitHub repository met:
   * `ai-generated` branch (jouw verbeterde versie)
   * `main` branch (originele code)
   * `prompts.md` (je prompt log)

Succes! Laat zien hoe jij AI als krachtig hulpmiddel gebruikt, zonder je kritische blik te verliezen.
