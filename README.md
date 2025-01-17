# Genuine Digital School - Proyecto Desplegable Prueba

## Descripción

Este proyecto facilita la interacción entre DialogFlow y el framework Laravel 11.



- **Credenciales:**
  - Email: admin2024@gmailcom
  - Contraseña: admin1234

## Tecnologías utilizadas

- Framework PHP Laravel 11
- PHP 8.2
- Vue 3 (integrado dentro del framework Laravel)
- JavaScript

## Agregación a un sitio personalizado

Si deseas agregar esta interacción a tu aplicación web en caso de ser util, agrega en tu html(personalizado acorde a tus necesidades):

<iframe height="430" width="350" src="https://bot.dialogflow.com/a91687cc-b3d3-4bfa-b1bc-e19ffb482f90"></iframe>


## Pasos de instalación en un entorno local

Si deseas implementar esta aplicación en tu entorno local, sigue estos pasos:

1. Clona el repositorio:

git clone https://github.com/dyeyo/school.git


2. Genera la clave de la aplicación y realiza las instalaciones necesarias:

```plaintext
composer install

npm install

3. Copia el archivo `.env.example` a `.env` y configura tu entorno local:

DB_CONNECTION=pgsql # o el de tu preferencia
DB_HOST=TU HOST
DB_PORT=TU PUERTO
DB_DATABASE=TU_DATABASE
DB_USERNAME=TU USERNAME
DB_PASSWORD=TU_PASSWORD

4. Genera la clave secreta para JWT y de laravel:

php artisan key:generate

php artisan jwt:secret


5. Ejecuta las migraciones y los seeders(usuario admin; como ejemplo: categorias y productos):

php artisan migrate --seed


6. Configura `vite.config.js` dentro de `resources/js/app.js`:

import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';
import vue from '@vitejs/plugin-vue';

export default defineConfig({
    plugins: [
        vue(),
        laravel({
            input: ['resources/css/app.css', 'resources/js/app.js'],
            refresh: true
        }),
    ],
});

7. Actualiza la configuración de axios en resources/js/app.js para el entorno local:

axios.defaults.baseURL = 'http://127.0.0.1:8000/api';

8. Inicia el servidor de desarrollo y el servidor de Laravel:

php artisan serve
npm run dev

9. Accede a la aplicación desde tu navegador:

Sitio principal: http://127.0.0.1:8000
Panel de administración: http://127.0.0.1:8000/admin

Saludos.
