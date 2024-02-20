# This Repository is a Clean Laravel 10 / FilamentPHP 3.2.25 Installation to Reproduce a Bug with Filament Actions and Reactivity

## Setup
Install the repository:

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan migrate:fresh --seed
```

Now go to `/admin/users` and Click "Open Action". Now try to type in the reactive field.

## Problem

Whenever the state within an Action Modal is updated, the Current User Input field loses its focus state.
