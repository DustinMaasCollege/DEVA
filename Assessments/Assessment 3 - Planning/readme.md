# Sollicitatie-opdracht 3 – ICT Support Ticket System Implementatie

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
* Welke tools en hulpmiddelen je hebt gebruikt voor je analyse
* Welke keuzes je bewust hebt gemaakt (en waarom)

### 2. Resultaat

Voor deze opdracht lever je een uitgewerkt technisch plan aan voor het implementeren van het meegeleverde prototype in een Laravel applicatie.

De focus ligt niet op "perfectie", maar op denkproces, aanpak en professionaliteit.

---

## De opdracht

In deze map vind je een [HTML prototype](./opdracht_3_prototype.html) van een ICT Support Ticket systeem voor Maas College. Dit prototype toont een ticket systeem met twee rollen:
- **Gebruikers**: kunnen tickets aanmaken
- **Managers**: kunnen tickets beheren en AI-gegenereerde reacties opstellen

Jouw taak is om een gedetailleerd technisch plan te schrijven voor de implementatie van dit prototype in een Laravel installatie.

### Functionaliteiten uit het prototype

Het prototype bevat de volgende functionaliteiten:
* **Ticket aanmaak formulier** met velden: naam, email, probleembeschrijving, gewenste oplossing
* **Dubbele interface**: gebruikers- en managerszicht via tabs
* **Ticket overzicht** voor managers met alle openstaande tickets
* **AI-integratie** voor het genereren van automatische reacties op tickets
* **Responsive design** met Tailwind CSS styling en Maas College branding

### Richtlijnen voor je technische plan

Beantwoord in je plan minimaal:

* **Scopebepaling**: Wat valt er wel en niet binnen deze feature? Welke delen van het prototype implementeer je?
* **Database design**: Welke tabellen en relaties heb je nodig voor tickets, gebruikers en reacties?
* **Technische aanpak**: 
   * Welke Laravel-componenten gebruik je (models, controllers, middleware, jobs, etc.)?
   * Welke packages of dependencies heb je nodig voor AI-integratie?
   * Hoe implementeer je de verschillende gebruikersrollen?
   * Hoe bouw je de frontend met Laravel en Tailwind CSS?
* **AI-integratie**: Hoe integreer je de AI-functionaliteit voor automatische reacties?
* **Authentication & Authorization**: Hoe onderscheid je tussen gebruikers en managers?
* **Tijdsinschatting**: Verdeel in user stories met realistische tijdsinschattingen
* **Risico's en obstakels**: Welke technische uitdagingen zie je vooraf?
* **Testing strategie**: Hoe test je tickets, AI-integratie en verschillende gebruikersrollen?
* **Beveiligingsoverwegingen**: Validatie, authorization, API-beveiliging

### Verwachte uitkomst

* Een uitgewerkt implementatieplan met:
   * **User stories** voor zowel gebruikers als managers (in story-formaat: "Als [rol] wil ik [functie] zodat [doel]")
   * **Database schema** met tabellen en relaties
   * **Technische architectuur** met onderbouwing van keuzes
   * **Subtasks** per user story voor development
   * **Tijdsinschatting** per story/subtask
   * **Risico-analyse** en mitigatie strategieën
* Optioneel maar gewaardeerd:
   * ERD (Entity Relationship Diagram) van de database
   * Wireframes of mockups voor Laravel views
   * API-documentatie voor AI-integratie
   * Deployment en configuratie overwegingen

### Structuur suggestie voor je plan

```markdown
# ICT Support Ticket System - Implementatieplan

## Executive Summary
Implementatie van het Maas College ICT Support Ticket systeem prototype in Laravel

## Scope
### In scope
- Ticket aanmaak door gebruikers
- Ticket beheer voor managers
- AI-gegenereerde reacties
- Gebruikersrollen (user/manager)
- Responsive Tailwind CSS frontend

### Out of scope
- Advanced rapportage functionaliteit
- Email notificaties
- File uploads bij tickets
- Multi-tenancy

## Database Schema
### Tabellen en relaties
- users (id, name, email, role, ...)
- tickets (id, user_id, title, description, status, ...)
- ticket_responses (id, ticket_id, generated_by, content, ...)

## User Stories

### Voor Gebruikers:
1. Als gebruiker wil ik een support ticket kunnen aanmaken zodat ik hulp kan krijgen van ICT
2. Als gebruiker wil ik mijn contactgegevens en probleem kunnen beschrijven zodat ICT mijn issue kan oplossen

### Voor Managers:
3. Als manager wil ik alle openstaande tickets kunnen zien zodat ik ze kan prioriteren
4. Als manager wil ik AI-gegenereerde reacties kunnen genereren zodat ik efficiënt kan reageren
5. Als manager wil ik tickets kunnen beheren zodat ik de status kan bijwerken

## Technische Uitwerking
### Laravel Componenten
- Models: User, Ticket, TicketResponse
- Controllers: TicketController, DashboardController  
- Middleware: RoleMiddleware
- Jobs: GenerateAIResponseJob (voor queue verwerking)

### Dependencies
- Laravel Breeze/Sanctum (authentication)
- HTTP Client voor AI API integratie
- Queue worker voor async AI calls

### Frontend
- Blade templates met Tailwind CSS
- Alpine.js voor interactiviteit
- Responsive design matching prototype

## AI Integratie
### Implementatie strategie
- Service class voor AI API communicatie
- Queue jobs voor async verwerking
- Error handling en fallback scenarios
- Rate limiting en cost management

## Risico's & Uitdagingen
- AI API kosten en rate limiting
- Performance bij veel tickets
- Security van AI API keys
- User experience tijdens AI processing

## Planning & Tijdsinschatting
### Sprint 1 (8 uur): Basis functionaliteit
- Database setup en models (2 uur)
- Authentication en rollen (2 uur) 
- Ticket CRUD functionaliteit (4 uur)

### Sprint 2 (6 uur): Frontend en AI
- Tailwind CSS styling (3 uur)
- AI integratie (3 uur)

### Sprint 3 (2 uur): Testing en polish
- Unit en feature tests (1 uur)
- Bug fixes en optimalisaties (1 uur)

## Testing Strategie
- Unit tests voor models en services
- Feature tests voor ticket workflows
- Browser tests voor UI functionaliteit
- AI integration mocking voor tests

## Beveiligingsoverwegingen
- Input validatie voor alle formulieren
- Authorization checks per rol
- CSRF protection
- AI API key security
- Rate limiting voor API calls
```

---

## Inleveren

* **Technisch plan** in Markdown formaat met bovenstaande structuur
* **User stories** uitgewerkt in subtasks voor zowel manager als gebruikerskant
* **Database ERD** (optioneel maar gewaardeerd)
* **Tijdsinschatting** per story/subtask voor realistische planning

**Geen werkende code vereist - focus ligt op technische planning en architectuur**

Succes!
