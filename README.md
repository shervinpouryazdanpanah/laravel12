# 🚀 Laravel GraphQL Livewire Starter

A modern Laravel 12 project powered by **Livewire 3**, **Volt**, **Tailwind CSS**, and a robust **GraphQL API** via **Lighthouse** and **GraphiQL**. This starter is designed for rapid frontend/backend development with real-time alerts, a reactive UI, and a fully extensible GraphQL backend.

---

## 📦 Included Packages

### Laravel Dependencies (`composer.json`)

| Package                       | Purpose                                                        |
| ----------------------------- | -------------------------------------------------------------- |
| `laravel/framework`           | Laravel 12 core framework.                                     |
| `laravel/tinker`              | REPL shell for Laravel. Useful for testing code interactively. |
| `livewire/livewire`           | Modern reactive components without leaving Laravel.            |
| `livewire/volt`               | Elegant Volt components (Livewire 3 syntax).                   |
| `jantinnerezo/livewire-alert` | SweetAlert2 wrapper for Livewire.                              |
| `nuwave/lighthouse`           | GraphQL server implementation for Laravel.                     |
| `mll-lab/laravel-graphiql`    | In-browser GraphiQL IDE for testing GraphQL queries.           |

### Frontend Tools (`package.json`)

| Package               | Purpose                                      |
| --------------------- | -------------------------------------------- |
| `vite`                | Frontend build tool with lightning-fast HMR. |
| `laravel-vite-plugin` | Integrates Vite with Laravel.                |
| `@tailwindcss/vite`   | Tailwind plugin for Vite.                    |
| `tailwindcss`         | Utility-first CSS framework.                 |
| `autoprefixer`        | Adds vendor prefixes to CSS.                 |
| `axios`               | HTTP client for API requests.                |
| `concurrently`        | Run Vite & Laravel server in parallel.       |

---

## ⚙️ Installation

```bash
git clone https://github.com/shervinpouryazdanpanah/laravel12.git
cd laravel12

# Install PHP dependencies
composer install

# Install frontend dependencies
npm install

# Build frontend assets
npm run dev

# Set up environment
cp .env.example .env
php artisan key:generate
```

---

## 🚀 Development Workflow

Start both Laravel and Vite in parallel:

```bash
concurrently "php artisan serve" "npm run dev"
```

This will start Laravel at `http://127.0.0.1:8000` and serve frontend assets via Vite.

---

## 🧩 Livewire, Volt & SweetAlert

Volt simplifies component building in Livewire:

```bash
php artisan make:volt-component Example
```

### SweetAlert Integration

Livewire Alert makes it easy to show user feedback with SweetAlert:

```php
$this->alert('success', 'Action completed!');
```

---

## 🧪 GraphQL with Lighthouse

### 📌 GraphQL Playground

After installing:

```bash
# Publish GraphiQL frontend assets
php artisan vendor:publish --tag=graphiql-assets
```

Visit:

```
http://localhost:8000/graphiql
```

### 📄 Example Query

```graphql
query {
    users {
        id
        name
        email
    }
}
```

---

## 🎨 Tailwind CSS

Tailwind CSS is fully integrated with Vite. You can start editing your styles in:

```
resources/css/app.css
```

Tailwind config is located at:

```
tailwind.config.js
```

---

## 📁 Folder Structure Tips

-   `resources/views/livewire`: Livewire Blade views
-   `app/GraphQL`: GraphQL queries, mutations, types
-   `app/Livewire`: Livewire classes
-   `resources/views/components`: Volt components
-   `routes/web.php`: Web routes
-   `routes/graphql.php`: GraphQL schema

---

## 🧼 Optional Commands

-   Clear caches:

    ```bash
    php artisan optimize:clear
    ```

-   Tailwind build (production):
    ```bash
    npm run build
    ```

---

## 📄 License

This project is open-sourced under the [MIT license](LICENSE).

---

## ✨ Credits

Crafted with ❤️ using Laravel, Livewire, and Tailwind by **Shervin Pouryazdanpanah**.

---

## 🔗 Helpful Links

-   [Laravel Documentation](https://laravel.com/)
-   [Livewire](https://livewire.laravel.com/)
-   [Volt](https://volt.laravel.com/)
-   [Lighthouse GraphQL](https://lighthouse-php.com/)
-   [Tailwind CSS](https://tailwindcss.com/)
