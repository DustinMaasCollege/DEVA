# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is **DEVA** - a recruitment assessment platform containing 4 independent Laravel-based coding assessments. The repository contains assessment documentation and ZIP packages with pre-configured Laravel starter projects.

**Language:** All documentation is in Dutch (Netherlands).

## Repository Structure

```
DEVA/
├── readme.md                                    # Main overview
└── Assessments/
    ├── readme - Install_instructions.md         # Universal setup guide
    ├── Assessment 1 - Roles/
    │   ├── readme.md
    │   ├── prompts and descriptions.md
    │   └── opdracht_1_rollen_rechten.zip
    ├── Assessment 2 - Bugfix/
    │   ├── readme.md
    │   ├── prompts and descriptions.md
    │   └── opdracht_2_bugfixing.zip
    ├── Assessment 3 - Planning/
    │   ├── readme.md
    │   ├── prompts and descriptions.md
    │   └── opdracht_3_prototype.html
    └── Assessment 4 - Prompting/
        ├── readme.md
        ├── prompts and descriptions.md
        └── opdracht_4_ai_prompting.zip
```

## Technology Stack

All Laravel packages use:

- **Backend Framework:** Laravel 12 (latest version)
- **Frontend Styling:** Tailwind CSS (utility-first CSS framework)
- **Templating Engine:** Blade
- **Frontend Framework:** Alpine.js (optional, for lightweight interactivity)
- **Build Tool:** Vite
- **Database:** MySQL/MariaDB (configured via Eloquent ORM)
- **Package Managers:** Composer (PHP), NPM (JavaScript)

## Laravel Package Structure

Each ZIP package contains a pre-configured Laravel 12 application with:

```
package/
├── install.sh                          # Automated setup script
├── .env.example                        # Database configuration template
├── composer.json                       # PHP dependencies (Laravel 12)
├── package.json                        # NPM dependencies
├── app/                                # Laravel application code
│   ├── Http/Controllers/
│   └── Models/
├── database/
│   ├── migrations/
│   └── seeders/
├── resources/
│   ├── css/
│   │   └── app.css                    # Tailwind CSS entry point
│   ├── js/
│   │   ├── app.js
│   │   └── bootstrap.js
│   └── views/                         # Blade templates
│       ├── layouts/
│       │   └── app.blade.php         # Master layout
│       ├── auth/
│       │   └── login.blade.php
│       ├── home.blade.php
│       ├── about.blade.php
│       └── data.blade.php
├── routes/
│   └── web.php                        # Route definitions
├── tailwind.config.js                 # Tailwind CSS configuration
├── vite.config.js                     # Vite build configuration
└── postcss.config.js                  # PostCSS configuration
```

## Common Development Commands

### Initial Setup (for extracted Laravel packages)

```bash
# Copy environment configuration
cp .env.example .env

# Edit .env and configure database:
# DB_DATABASE=laravel_opdracht
# DB_USERNAME=root
# DB_PASSWORD=your_password

# Create database in MySQL
mysql -u root -p
CREATE DATABASE laravel_opdracht;

# Run automated installation
chmod +x install.sh
./install.sh

# OR manually install dependencies
composer install
php artisan key:generate
php artisan migrate
php artisan db:seed
npm install
npm run build
```

### Running the Application

```bash
# Start development server
php artisan serve
# Access at http://localhost:8000

# Default test credentials (if seeded)
# Email: jd@maascollege.nl
# Password: MijnDevelopmentOpdracht0@!
```

### Development Workflow

```bash
# Run migrations
php artisan migrate

# Reset database and re-run migrations
php artisan migrate:fresh

# Run database seeders
php artisan db:seed

# Run specific seeder
php artisan db:seed --class=UserSeeder

# Install PHP dependencies
composer install

# Install JavaScript dependencies
npm install

# Build assets for production
npm run build

# Build assets for development with hot reload
npm run dev

# Clear application cache
php artisan cache:clear

# Clear configuration cache
php artisan config:clear

# Clear route cache
php artisan route:clear

# Clear view cache
php artisan view:clear

# Run all cache clearing commands at once
php artisan optimize:clear
```

### Testing

```bash
# Run all tests
php artisan test

# Run specific test file
php artisan test --filter TestClassName

# Run tests with coverage
php artisan test --coverage
```

### Code Quality

```bash
# Laravel Pint (code style fixer) if installed
./vendor/bin/pint

# PHPStan (static analysis) if installed
./vendor/bin/phpstan analyse
```

## System Requirements

- PHP 8.2 or higher
- Composer
- Node.js & NPM
- MySQL/MariaDB or compatible database

## Architecture Patterns

The Laravel packages follow standard Laravel conventions:

- **MVC Pattern:** Models, Views (Blade), Controllers
- **Eloquent ORM:** For database interactions
- **Blade Templating:** For views with master layouts
- **Route Definitions:** In `routes/web.php`
- **Migrations:** For database schema management
- **Seeders:** For test data population

## Security Features (Pre-configured)

- CSRF token protection on forms
- Password hashing with bcrypt
- Input validation capabilities
- SQL injection prevention via Eloquent ORM
- XSS protection in Blade templates

## Frontend Setup

**Tailwind CSS** is fully configured and uses:
- Utility-first CSS approach
- Configuration in `tailwind.config.js`
- Compiled via Vite build tool
- Custom styles can be added to `resources/css/app.css`

**Vite** handles:
- Asset compilation
- Hot module replacement in development
- Production builds with optimization
