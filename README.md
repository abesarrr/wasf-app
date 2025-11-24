# WASF PHP Framework — Extended Edition 🚀

![Badge](https://img.shields.io/badge/WASF-Framework-blue)
![Badge](https://img.shields.io/badge/WASF-v3.1.5-red)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Stable-brightgreen)
![PHP](https://img.shields.io/badge/PHP-8.1%2B-purple)

---

# 📸 Screenshot

![App Screenshot](https://github.com/abesarrr/wasf-app/blob/main/Welcome-Wasframwork-11-24-2025_06_03_PM.png?raw=true)

---

# 🧬 Arsitektur WASF (Diagram)

```mermaid
graph TD
    A[public/index.php] --> B[Bootstrap]
    B --> C[Routing]
    C --> D[Controller]
    D --> E[Model]
    D --> F[View]
    E --> G[Database Layer]
    F --> H[WASF Templating]
```

---

# ✨ Fitur Utama

* Super Lightweight & Fast  
* HMVC Modular Architecture  
* Blade Templating Engine  
* WASF Console Commands  
* PDO Database Wrapper  
* .env Loader & Config Manager  
* PSR-4 Autoloading  
* Extendable & Clean Structure  

---

# ⚡ Instalasi

## Opsi 1 — WASF Installer

```bash
composer global require wasframework/wasf-installer
wasf new myproject
cd myproject
```

## Opsi 2 — Composer

```bash
composer create-project wasframework/wasf-app myproject
cd myproject
```

---

# 🔑 Setup Aplikasi

```bash
cp .env.example .env
php wasf key:generate
php wasf serve
```

Akses:  
`http://localhost:8000`

---

# 🧱 Struktur Direktori

```txt
app/
 ├─ Controllers/
 ├─ Models/
 └─ Views/
Modules/
routes/
public/
storage/
```

---

# 🧪 Migration Example

```php
<?php

use Wasf\Database\Schema;

return new class {
    public function up()
    {
        Schema::create("users", function($t){
            $t->id();
            $t->string("name");
            $t->string("username")->unique();
            $t->string("email")->unique();
            $t->string("password");
            $t->string("photo")->default("/uploads/profile/default.png");
            $t->timestamps();
        });
    }

    public function down()
    {
        Schema::dropIfExists("users");
    }
};
```

---

# 🔧 CLI Commands

```bash
php wasf make:controller UserController
php wasf make:model User
php wasf make:migration create_users_table
php wasf migrate
php wasf route:list
php wasf clear:view
```

---

# 🛡 Keamanan

Kontak: **wasuryanto3@gmail.com**

---

# 📄 Lisensi

MIT License
