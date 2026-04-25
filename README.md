# DS7-CrudLaravel

## Introducción

Este laboratorio consiste en desarrollar un sistema CRUD (Crear, Leer, Actualizar y Eliminar) en Laravel utilizando la arquitectura Modelo Vista Controlador (MVC). Se implementó la gestión de productos con operaciones completas sobre la base de datos.

## Arquitectura MVC

* Modelos: manejan la base de datos (Product)
* Vistas: interfaces para el usuario (Blade)
* Controladores: lógica del sistema (ProductController)
* Rutas: navegación del sistema

## Requisitos

* <a href="https://www.php.net/" target="_blank">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" width="20"/> PHP 8
  </a>  

* <a href="https://getcomposer.org/" target="_blank">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/composer/composer-original.svg" width="20"/> Composer
  </a>  

* <a href="https://laravel.com/" target="_blank">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg" width="20"/> Laravel
  </a>  

* <a href="https://www.mysql.com/" target="_blank">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="20"/> MySQL
  </a>  

* <a href="https://code.visualstudio.com/" target="_blank">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" width="20"/> Visual Studio Code
  </a>  

* <a href="https://www.npmjs.com/" target="_blank">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/npm/npm-original-wordmark.svg" width="20"/> NPM
  </a>  

* Sistema Operativo: Windows 10 o superior

## Comandos utilizados

* composer create-project laravel/laravel crud_rapido
* composer require ibex/crud-generator --dev
* php artisan make:model Product -m
* php artisan migrate:fresh
* php artisan vendor:publish --tag=crud
* php artisan make:crud products
* npm install
* npm run dev
* php artisan serve

## Base de Datos

Se utilizó MySQL configurado en el archivo `.env`:

* DB_DATABASE=crud_laravel
* DB_USERNAME=root
* DB_PASSWORD=

## Estructura de la tabla

La tabla `products` contiene los siguientes campos:

* id
* description
* price
* stock
* created_at
* updated_at

## Resultado

Página del Crud
![CRUD](CrudV.png)

Formulario de creación
![CRUD](CrudCreate.png)
![CRUD](CrudCreate2.png)

Página del Crud (con contenido)
![CRUD](CrudLLeno.png)

Crud Show
![CRUD](CrudShow.png)
![CRUD](CrudShow2.png)

Edición de producto
![CRUD](crud3.png)

Crud Delete
![CRUD](CrudDelete.png)
![CRUD](CrudDelete2.png)

## Dificultades y Soluciones

### Problema 1: Error "table already exists"

La tabla ya existía al ejecutar migraciones.

**Solución:**
Se utilizó el comando `php artisan migrate:fresh` para reiniciar la base de datos.

---

### Problema 2: Advertencia con tipo double

VS Code mostraba error en `$table->double()`.

**Solución:**
Se cambió a `$table->decimal('price', 8, 2)` para mayor precisión.

---

## Referencias

* https://laravel.com/docs
* https://www.php.net/
* https://getcomposer.org/

## Fecha de Ejecución

25 de abril de 2026

---

Este laboratorio ha sido desarrollado por el estudiante de la Universidad Tecnológica de Panamá:

Nombre: Gustavo Domínguez
Correo: gustavo.dominguez1@utp.ac.pa
Curso: Desarrollo de Software VII
Instructor del Laboratorio: Irina Fong
