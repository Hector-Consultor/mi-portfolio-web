---
created: 2026-03-06T22:51:53Z
last_updated: 2026-03-06T22:51:53Z
version: 1.0
author: Claude Code PM System
---

# Contexto tecnológico

## Stack

| Tecnología | Versión | Uso |
|------------|---------|-----|
| HTML5 | — | Estructura semántica |
| CSS3 + Variables | — | Estilos con design tokens |
| JavaScript | ES6+ vanilla | Animaciones, UI, canvas |

**Sin frameworks. Sin dependencias. Sin npm. Sin build step.**

## CSS Variables (Design Tokens)

Definidas en `:root`:

```css
--bg:          #0a0a0f    /* fondo principal */
--bg2:         #111118    /* fondo secundario */
--bg3:         #1a1a24    /* fondo terciario (cards) */
--border:      #2a2a3a    /* bordes */
--accent:      #6c63ff    /* violeta principal */
--accent2:     #00d4ff    /* cyan secundario */
--text:        #e8e8f0    /* texto principal */
--text-muted:  #8888aa    /* texto secundario */
--radius:      12px       /* border-radius global */
--transition:  0.3s ease  /* transición global */
```

## Fuentes
- **Sistema:** `'Segoe UI', system-ui, -apple-system, sans-serif`
- Sin Google Fonts ni carga externa — mejora performance

## Canvas API (JavaScript)
El proyecto hace uso extensivo de la Canvas API:
- **Hero canvas:** partículas animadas con efecto de repulsión al mouse
- **Mini canvases decorativos:** íconos animados en cards de servicios y sección Sobre mí

## Responsive
- **Enfoque:** mobile-first
- **Breakpoints:** `768px` (tablet) · `480px` (móvil pequeño)
- No usa CSS Grid frameworks — grid nativo CSS

## Deploy & hosting
- **Plataforma:** Netlify (plan gratuito)
- **Trigger:** push a rama `main` en GitHub → deploy automático en ~30 segundos
- **URL:** https://hgautomation.netlify.app
- **Repositorio:** https://github.com/Hector-Consultor/mi-portfolio-web

## Herramientas de desarrollo
- **IDE:** VS Code
- **Asistente:** Claude Code (Sonnet 4.6)
- **Git:** GitHub Desktop / CLI
- **Preview local:** Live Server (extensión VS Code) o `python -m http.server 8080`
- **Comandos slash disponibles:** `/deploy` · `/revisar` · `/seo`
