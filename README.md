# Terra Viajes

Sitio institucional estático (HTML + SASS) — proyecto final.

## Estructura

```
terra/
├── index.html              ← única página en la raíz
├── styles.css              ← CSS COMPILADO (lo que usa el navegador)
├── pages/
│   ├── destinos.html
│   ├── tours.html
│   ├── nosotros.html
│   └── contacto.html
├── images/                 ← acá van tus imágenes
└── scss/                   ← código fuente de los estilos
    ├── main.scss           ← punto de entrada (importa todo)
    ├── abstracts/          ← _variables, _mixins, _placeholders
    ├── base/               ← _reset, _base
    ├── layout/             ← _header (header + nav + footer)
    ├── components/         ← _buttons, _cards, _forms
    └── pages/              ← _home, _destinos, _nosotros, _contacto, _tours
```

## Imágenes necesarias (carpeta `images/`)

- `terra_logo_wordmark.svg`
- `patagonia.jpg`
- `japon.jpg`
- `brasil.jpg`
- `marruecos.jpg`
- `islandia.avif`
- `peru.jpg`
- `nosotros.webp`

## Compilar el SASS

Si modificás algo en `scss/`, recompilá el CSS con:

```bash
sass scss/main.scss styles.css
```

O en modo "watch" (recompila solo al guardar):

```bash
sass --watch scss/main.scss:styles.css
```

> El `styles.css` ya viene compilado, así que el sitio funciona sin necesidad
> de compilar nada para verlo o subirlo.

## Características

- HTML semántico (`header`, `nav`, `main`, `section`, `article`, `footer`).
- SEO: `lang="es"`, `meta description`, `keywords`, `author`, `robots` y Open Graph.
- SASS con variables, mixins, placeholders (`@extend`), nesting y partials (7-1).
- Responsive (breakpoints en 900px y 600px vía mixin `responde`).
- Animaciones: transiciones y `transform` en hover + librería AOS (fade-up al scrollear).

## Deploy (Netlify / Vercel)

1. Subí la carpeta a un repo de GitHub.
2. En Netlify/Vercel: "Import" del repo.
3. No requiere build (es estático): dejá el comando de build vacío y el
   directorio de publicación en la raíz (`/`).
