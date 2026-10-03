# SPEKTRA — Internship Management System

SPEKTRA is a Laravel application for coordinating student internship (PKL) placements. The implemented web flows focus on students and coordinators, from submitting and reviewing placements to monitoring and reporting.

## Current features

- Student and coordinator accounts with role-based access
- Student internship registration with supporting document uploads
- Coordinator review, approval, and rejection of registrations
- Company and student views for internship placements
- Internship monitoring pages and report views
- Authentication, password reset, notifications, and activity records

The repository also defines API resource routes. Some API resource controllers are incomplete, so the web application is the primary implemented interface.

## Stack

- PHP 8.2+
- Laravel 12
- SQLite or another database supported by Laravel
- Node.js and npm with Vite

## Run locally

    git clone https://github.com/Rimaestro/spektra-internship-management.git
    cd spektra-internship-management
    composer install
    npm install

Copy .env.example to .env and configure the database:

    # Windows PowerShell
    Copy-Item .env.example .env

    # macOS/Linux
    # cp .env.example .env

    php artisan key:generate
    php artisan migrate --seed
    npm run build
    php artisan serve

Open http://127.0.0.1:8000. The seeders create sample accounts and records with shared development passwords. Use them only in a local database and change all credentials before any deployment.

## Tests

    php artisan test

The repository also contains a Playwright end-to-end test under tests/E2E/. Review its configuration before running it.

## Documentation

- docs/README.md — project documentation index
- docs/diagrams/README.md — diagrams documentation
- docs/analisis-kebutuhan-sistem.md — original system analysis and requirements

## Project structure

- app/Http/Controllers/ — student, coordinator, authentication, and API flows
- app/Models/ — internship, company, report, evaluation, and user records
- database/migrations/ — schema
- resources/views/ — web interface
- routes/ — web and API routes
- tests/ — feature, unit, and end-to-end tests

## License

No license file is currently included. Reuse and redistribution are not granted unless the project owner adds a license.

