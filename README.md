# Proyecto Hostal Torrecillas Blancas - Refactorización de Imágenes

Este documento describe el proceso para actualizar la página web del Hostal Torrecillas Blancas, moviendo las imágenes de servicios externos a una carpeta local del proyecto.

## Objetivo

El objetivo principal es mejorar el rendimiento, la mantenibilidad y la independencia del sitio web al dejar de usar URLs absolutas de servicios como Imgur o Wix. En su lugar, se utilizarán rutas relativas a una carpeta local `/images`.

## Tareas a Realizar

### 1. Estructura de Carpetas Recomendada 📂

Se creará una nueva carpeta llamada `images` en la raíz del proyecto. La estructura final será:

```
/torrecillas-blancas/
├── index.html
├── README.md
└── /images/
    ├── hero-t1.jpeg
    ├── suite-delta-1.jpeg
    ├── suite-delta-2.jpeg
    ├── suite-delta-3.jpeg
    ├── suite-delta-4.jpeg
    ├── rincon-1.jpeg
    ├── rincon-2.jpeg
    ├── rincon-3.jpeg
    ├── rincon-4.jpeg
    ├── refugio-1.jpeg
    ├── refugio-2.jpeg
    ├── refugio-3.jpeg
    ├── refugio-4.jpeg
    ├── logo.png
    └── favicon.png
```

### 2. Descarga de Imágenes

Todas las imágenes que actualmente se cargan desde `i.imgur.com`, `static.wixstatic.com` y `placehold.co` serán descargadas y guardadas en la nueva carpeta `/images` con los nombres de archivo correspondientes.

### 3. Actualización de Rutas en `index.html`

Se modificarán todas las referencias a imágenes en el archivo `index.html` para que apunten a las rutas locales relativas. Esto incluye:

- **Logo y Favicon:** Se actualizarán las etiquetas `<link>` y `<img>`.
- **Imagen Hero:** Se modificará el `background-image` en la sección principal.
- **Imágenes de Habitaciones:** Se cambiarán los `src` de las imágenes principales de cada habitación.
- **Galería en JavaScript:** Se actualizarán las URLs en el objeto `roomData` para la galería modal.

Este proceso asegurará que el proyecto sea autocontenido y más fácil de mantener en el futuro.