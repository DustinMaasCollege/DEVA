# Laravel 12 Sollicitatie Opdrachten - Complete Pakketten

## 📦 Wat heb je ontvangen?

Je hebt 7 bestanden ontvangen:

### Opdracht Documenten (Markdown bestanden)
1. **[Home](./../readme.md).md** - Overzicht van alle 4 opdrachten
2. **[Opdracht 1 // Rollen & Rechten](./Assessment%201%20-%20Roles/readme.md)** - Volledige opdracht beschrijving #1
3. **[Opdracht 2 // Bugfixing](./Assessment%202%20-%20Bugfix/readme.md)** - Volledige opdracht beschrijving #2
4. **[Opdracht 3 // Planmatig werken](./Assessment%203%20-%20Planning/readme.md)** - Volledige opdracht beschrijving #3
5. **[Opdracht 4 // AI Prompting](./Assessment%204%20-%20Prompting/readme.md)** - Volledige opdracht beschrijving #4

### Laravel Starter Pakketten (ZIP bestanden)
2. **opdracht_1_rollen_rechten.zip** - Laravel pakket voor opdracht 1
3. **opdracht_2_bugfixing.zip** - Laravel pakket voor opdracht 2 (met bugs!)
4. **opdracht_3_prototype.html** - Prototype van design
5. **opdracht_4_ai_prompting.zip** - Laravel pakket voor opdracht 4

## 🎯 Welk pakket gebruik je?

### Opdracht 1: Rollen & Rechten
- **Gebruik:** `opdracht_1_rollen_rechten.zip`
- **Bevat:** Clean Laravel 12 setup
- **Jouw taak:** Bouw een rollen & rechten systeem

### Opdracht 2: Bugfixing & Debugging
- **Gebruik:** `opdracht_2_bugfixing.zip`
- **Bevat:** Laravel 12 setup **met bugs erin!**
- **Jouw taak:** Vind en fix alle bugs

### Opdracht 3: Planuitwerking
- **Gebruik:** Figma design link
- **Jouw taak:** Schrijf een technisch plan voor de ontwikkeling van het Figma design

### Opdracht 4: AI-Assisted Development
- **Gebruik:** `opdracht_4_ai_prompting.zip`
- **Bevat:** Clean Laravel 12 setup
- **Jouw taak:** Gebruik AI om code te genereren en beoordeel deze kritisch

## 📂 Wat zit er in elk Laravel pakket?

Alle pakketten bevatten:

```
pakket/
├── install.sh              # Automatisch installatie script
├── .env.example           # Database configuratie template
├── .gitignore             # Git ignore file
├── composer.json          # PHP dependencies
├── package.json           # NPM dependencies
├── README.md              # Basis installatie instructies
├── OPDRACHT.md            # Specifieke opdracht instructies
│
├── app/
│   ├── Http/Controllers/Auth/
│   │   └── AuthenticatedSessionController.php
│   └── Models/
│       └── User.php
│
├── database/
│   ├── migrations/
│   │   └── 0001_01_01_000000_create_users_table.php
│   └── seeders/
│       └── DatabaseSeeder.php
│
├── resources/
│   ├── css/
│   │   └── app.css (Tailwind CSS)
│   ├── js/
│   │   ├── app.js
│   │   └── bootstrap.js
│   └── views/
│       ├── layouts/
│       │   └── app.blade.php
│       ├── auth/
│       │   └── login.blade.php
│       ├── home.blade.php
│       ├── about.blade.php
│       └── data.blade.php
│
├── routes/
│   └── web.php
│
├── tailwind.config.js
├── vite.config.js
└── postcss.config.js
```

## 🚀 Snelstart Gids

### Stap 1: Kies je opdracht
Lees eerst de opdracht beschrijvingen in de markdown bestanden.

### Stap 2: Pak het juiste ZIP bestand uit
```bash
# Bijvoorbeeld voor opdracht 1:
unzip opdracht_1_rollen_rechten.zip
cd opdracht_1_pakket
```

### Stap 3: Configureer database
1. Open `.env.example`
2. Pas database instellingen aan:
   ```
   DB_DATABASE=laravel_opdracht
   DB_USERNAME=root
   DB_PASSWORD=jouw_wachtwoord
   ```
3. Maak de database aan in MySQL:
   ```sql
   CREATE DATABASE laravel_opdracht;
   ```

### Stap 4: Voer installatie script uit
```bash
# Linux/Mac:
chmod +x install.sh
./install.sh

# Windows (met Git Bash):
bash install.sh
```

Of handmatig:
```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan db:seed
npm install
npm run build
```

### Stap 5: Start de applicatie
```bash
php artisan serve
```

Open in browser: http://localhost:8000

### Stap 6: Login met test account
- **Email:** jd@maascollege.nl
- **Wachtwoord:** MijnDevelopmentOpdracht0@!

## 🎨 Wat is er al vooraf gemaakt?

Elk pakket heeft:
- ✅ Laravel 12 (nieuwste versie)
- ✅ Tailwind CSS volledig geconfigureerd
- ✅ 3 werkende pagina's (Home, Over Ons, Belangrijke Gegevens)
- ✅ Authentication systeem (login/logout)
- ✅ Test gebruiker met credentials
- ✅ Responsive layout met navigatie
- ✅ Database migrations en seeders
- ✅ Alle beveiligingsmaatregelen (CSRF, XSS, etc.)

## 📝 Verschillen per pakket

### Opdracht 1 Pakket (Clean)
- Geen speciale aanpassingen
- Klaar om je rollen & rechten systeem aan toe te voegen

### Opdracht 2 Pakket (Buggy! 🐛)
- Bevat **opzettelijk** bugs in `resources/views/data.blade.php`
- Let op: Logic errors, performance issues, en code organization problemen
- Jouw taak: vind en fix ze!

### Opdracht 4 Pakket (Clean)
- Geen speciale aanpassingen
- Klaar om je AI-gegenereerde features aan toe te voegen

## ⚙️ Vereisten

Zorg dat je het volgende hebt geïnstalleerd:
- **PHP 8.2+** (check: `php -v`)
- **Composer** (check: `composer -V`)
- **Node.js & NPM** (check: `node -v` en `npm -v`)
- **MySQL/MariaDB** of andere database

## 🐛 Problemen oplossen?

### "Composer not found"
Installeer Composer: https://getcomposer.org

### "NPM not found"
Installeer Node.js: https://nodejs.org

### "SQLSTATE connection refused"
1. Check of je database server draait
2. Verifieer je `.env` database credentials
3. Zorg dat de database `laravel_opdracht` bestaat

### "Vite manifest not found"
Voer `npm run build` uit

### Permission errors op Linux/Mac
```bash
chmod +x install.sh
sudo chmod -R 777 storage bootstrap/cache
```

## 📚 Handige Links

- [Laravel 12 Documentatie](https://laravel.com/docs)
- [Tailwind CSS Documentatie](https://tailwindcss.com/docs)
- [PHP Documentatie](https://www.php.net/docs.php)
- [Composer Documentatie](https://getcomposer.org/doc/)

## 💡 Tips

1. **Gebruik Git:** Initialiseer een repository en commit regelmatig
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **Lees BEIDE README's:**
   - `README.md` = Basis installatie instructies
   - `OPDRACHT.md` = Specifieke opdracht requirements

3. **Test grondig:** Probeer verschillende scenario's

4. **Documenteer je werk:** Voeg comments toe, maak een SOLUTION.md

5. **Gebruik moderne tools:** AI, Stack Overflow, documentatie - alles mag!

## ❓ Vragen?

Bij problemen:
1. Check de foutmeldingen zorgvuldig
2. Lees de README.md in het pakket
3. Gebruik Stack Overflow of Laravel forums
4. Gebruik AI-tools voor debugging (ChatGPT, Claude, Cursor)

## ✅ Klaar om te beginnen?

1. ✅ Kies je opdracht
2. ✅ Pak het juiste ZIP bestand uit
3. ✅ Volg de installatie stappen
4. ✅ Lees de OPDRACHT.md
5. ✅ Start met coderen!

Veel succes met je opdracht! 🚀💻

---

**Gemaakt voor:** Maas College Sollicitatie Proces  
**Laravel Versie:** 12.x  
**Datum:** December 2024  
