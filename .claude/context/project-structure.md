---
created: 2026-03-06T22:51:53Z
last_updated: 2026-03-06T22:51:53Z
version: 1.0
author: Claude Code PM System
---

# Estructura del proyecto

## Directorio raíz

```
mi-primera-web/
├── index.html              # Archivo único: HTML + CSS + JS embebidos
├── foto-hector.png         # Foto de perfil del propietario
├── README.md               # Documentación del proyecto con badges
├── CLAUDE.md               # Contexto para Claude Code
├── .gitignore
├── .claude/
│   ├── settings.json       # Config de Claude Code (MCP, permisos)
│   ├── settings.local.json # Config local (no commitear)
│   ├── context/            # Archivos de contexto (este directorio)
│   └── commands/
│       ├── deploy.md       # Skill /deploy
│       ├── revisar.md      # Skill /revisar
│       └── seo.md          # Skill /seo
```

## Arquitectura del index.html

El proyecto es un **single-file**: todo el CSS, HTML y JavaScript está en `index.html`. Estructura interna:

```
index.html
├── <head>
│   ├── meta SEO (description, viewport, charset)
│   ├── title
│   └── <style> — todo el CSS (~900 líneas)
│       ├── Reset & CSS Variables (:root)
│       ├── Utilities (.container, .section-label, etc.)
│       ├── Navbar (#navbar, .nav-links, hamburger)
│       ├── Mobile menu (.mobile-menu)
│       ├── Hero (#hero, canvas, .hero-content)
│       ├── Sobre mí (#sobre-mi, .about-grid)
│       ├── Servicios (#servicios, .services-grid)
│       ├── Proyectos (#proyectos, .projects-grid)
│       ├── Tecnologías (#tecnologias, .tech-grid)
│       ├── Contacto (#contacto, .contact-links)
│       ├── Footer
│       ├── Animaciones (@keyframes)
│       └── Responsive (768px, 480px)
└── <body>
    ├── <nav id="navbar">
    ├── <div class="mobile-menu">
    ├── <section id="hero">          — Canvas de partículas
    ├── <section id="sobre-mi">      — Foto + texto + diferenciadores
    ├── <section id="servicios">     — 3 cards de servicios
    ├── <section id="proyectos">     — Casos de éxito
    ├── <section id="tecnologias">   — Grid de tecnologías
    ├── <section id="contacto">      — Links de contacto
    ├── <footer>
    └── <script>                     — JavaScript (~400 líneas)
        ├── Canvas Hero (partículas interactivas)
        ├── Canvas decorativos (mini canvases en cards)
        ├── Navbar scroll effect
        ├── Hamburger menu
        ├── Smooth scroll
        └── Intersection Observer (animaciones fade-up)
```

## Convención de IDs de sección

| ID HTML | Enlace navbar | Descripción |
|---------|--------------|-------------|
| `#hero` | — | Pantalla de bienvenida |
| `#sobre-mi` | Sobre mí | Perfil profesional |
| `#servicios` | Servicios | Cards de servicios |
| `#proyectos` | Proyectos | Casos de éxito |
| `#tecnologias` | Tecnologías | Stack de herramientas |
| `#contacto` | Contacto | Links de contacto |
