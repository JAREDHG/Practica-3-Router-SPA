# Práctica 3: Sistema SPA con Vue Router y Laravel Sanctum

Proyecto desarrollado para la asignatura de Desarrollo Web, enfocado en la implementación de una **Single Page Application (SPA)** con navegación dinámica, gestión de estado y autenticación protegida.

## Descripción del Proyecto
Este sistema permite la gestión de un catálogo de productos con una arquitectura desacoplada (Frontend en Vue 3, Backend en Laravel). El acceso a las funcionalidades administrativas está protegido mediante un sistema de **Guards** en el cliente y **Middleware** de autenticación en el servidor.

## Tecnologías Utilizadas

### Frontend
- **Vue 3 (Vite):** Framework progresivo para la interfaz.
- **Vue Router:** Gestión de rutas y navegación SPA.
- **Axios:** Consumo de servicios RESTful.
- **Bootstrap 5:** Diseño responsivo y componentes de UI.

### Backend
- **Laravel 10:** API RESTful.
- **Laravel Sanctum:** Protección de rutas y gestión de tokens.
- **MariaDB:** Base de datos relacional.

## Características Principales
- **Navegación Fluida:** SPA implementada para evitar recargas de página.
- **Control de Acceso:** Uso de `beforeEach` para proteger rutas administrativas y redirigir usuarios no autenticados.
- **Dashboard Administrativo:** Panel de monitoreo con métricas de red y estado del servidor.
- **API Segura:** Endpoints protegidos mediante Sanctum.

## ⚙️ Instrucciones de Instalación
1. **Backend:** 'cd backend', 'composer install', 'php artisan migrate', 'php artisan serve'.
2. **Frontend:** 'cd frontend', 'npm install', 'npm run dev'.

**Desarrollado por:** Jared Hernández González - Universidad Politécnica de Texcoco (UPTex)