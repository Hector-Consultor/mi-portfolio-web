---
created: 2026-03-06T22:51:53Z
last_updated: 2026-03-06T22:51:53Z
version: 1.0
author: Claude Code PM System
---

# Patrones del sistema

## Arquitectura general
**Single-file web app** — todo el código vive en `index.html`. Decisión consciente para un portfolio estático: sin build step, sin dependencias, máxima portabilidad.

## Patrones CSS

### Design Tokens via CSS Variables
Todos los colores, radios y transiciones están centralizados en `:root`. Para cambiar el tema completo basta modificar esas variables.

### Clases utilitarias reutilizables
```css
.container       /* max-width 1100px, centrado, padding 24px */
.section         /* padding vertical estándar de secciones */
.section-header  /* cabecera de sección con label + title + desc */
.section-label   /* etiqueta cyan uppercase */
.section-title   /* título principal de sección */
.section-desc    /* descripción en gris */
.fade-up         /* elemento que se anima al entrar en viewport */
```

### Nomenclatura de IDs
IDs de sección en español con guión: `#sobre-mi`, `#servicios`, `#proyectos`, `#tecnologias`, `#contacto`.

## Patrones JavaScript

### Intersection Observer para animaciones
Las clases `.fade-up` se activan cuando el elemento entra en el viewport. No hay animaciones en elementos fuera de pantalla.

```javascript
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
```

### Canvas API — partículas
El hero canvas genera partículas con:
- Posición y velocidad random al init
- Efecto de repulsión cuando el mouse se acerca
- Líneas entre partículas cercanas
- Loop con `requestAnimationFrame`

### Canvas decorativos en cards
Cada card de servicios y cada diferenciador en "Sobre mí" tiene un mini canvas con un icono animado específico. Se inicializan en `DOMContentLoaded`.

### Navbar scroll effect
Event listener en `window scroll` que agrega/quita clase `.scrolled` al `#navbar` para aplicar fondo semitransparente con blur.

### Stagger animations en tecnologías
Las cards del stack de herramientas tienen `animation-delay` escalonado para el efecto de aparición en cascada.

## Patrones de contenido

### Cards de servicios
Estructura uniforme: canvas decorativo → título → descripción → lista de features → badge de herramientas.

### Sección tecnologías
Grid de iconos con nombre y categoría. Agrupados por área: Automatización · Low-code Microsoft · Google Workspace · RPA empresarial · IA.

## Patrones a mantener al agregar código
1. Usar siempre las CSS Variables — nunca hardcodear colores
2. Mantener comentarios de sección en CSS: `/* ─── Nombre ─── */`
3. Nuevas secciones siguen el patrón: `<section id="nombre" class="section">`
4. Imágenes externas: ninguna — todo es CSS/Canvas para evitar dependencias
5. No agregar librerías externas sin discutir primero
