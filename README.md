# Portafolio Académico — Herramientas de Programación 4

Sitio estático para GitHub Pages. No requiere instalación ni build: es HTML puro.

## Estructura de carpetas

```
edu6441.github.io/
├── index.html
└── assets/
    ├── pdfs/
    │   ├── examen-parcial-1.pdf
    │   ├── examen-parcial-2.pdf
    │   ├── investigacion-1.pdf
    │   ├── investigacion-2.pdf
    │   ├── taller-practico-1.pdf
    │   ├── taller-practico-2.pdf
    │   ├── ejercicio-practico-1.pdf
    │   ├── ejercicio-practico-2.pdf
    │   └── ejercicio-practico-3.pdf
    └── apps/
        ├── examen-parcial-1.zip
        ├── examen-parcial-2.zip
        ├── taller-practico-1.zip
        ├── taller-practico-2.zip
        ├── ejercicio-practico-1.zip
        ├── ejercicio-practico-2.zip
        └── ejercicio-practico-3.zip
```

> Las investigaciones **no llevan carpeta de app**, ya que en esos trabajos no se desarrolló ninguna aplicación.

## Cómo agregar tus trabajos

1. Coloca cada PDF dentro de `assets/pdfs/` usando **exactamente** el mismo nombre de archivo que aparece arriba (o cambia el nombre en `index.html`, ver más abajo).
2. Si el trabajo tiene una app (proyecto de código), comprímela en `.zip` y colócala en `assets/apps/` con el mismo nombre base.
3. Sube los cambios a GitHub:

```bash
git add .
git commit -m "Agrego PDFs y apps de los trabajos"
git push
```

4. Espera 1-2 minutos y actualiza `https://edu6441.github.io` — mientras no subas el PDF correspondiente, la página mostrará automáticamente el aviso "Todavía no se subió el PDF para este trabajo."

## Cómo agregar o editar un trabajo

Toda la información de los trabajos está en un solo lugar dentro de `index.html`, en el bloque `const DATA = {...}` (cerca de la etiqueta `<script>`). Cada trabajo tiene esta forma:

```js
{ id: "parcial1", title: "Examen Parcial 1", pdf: "assets/pdfs/examen-parcial-1.pdf", app: "assets/apps/examen-parcial-1.zip" }
```

- `title`: el texto que se muestra en el menú y en el panel principal.
- `pdf`: la ruta al archivo PDF.
- `app`: la ruta al archivo de la app, o `null` si no aplica (como en investigaciones).

Para agregar un trabajo nuevo, copia una línea existente dentro de la categoría correspondiente y cambia los valores.

## Categorías incluidas

- Parciales (2)
- Investigaciones (2) — sin descarga de app
- Talleres (2)
- Ejercicios (3)
