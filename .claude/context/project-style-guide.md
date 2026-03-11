---
created: 2026-03-06T22:51:53Z
last_updated: 2026-03-06T22:51:53Z
version: 1.0
author: Claude Code PM System
---

# Guía de estilo

## Colores (siempre via CSS Variables)

| Variable | Valor | Uso |
|----------|-------|-----|
| `var(--accent)` | `#6c63ff` | Violeta — acción principal, hover, scrollbar |
| `var(--accent2)` | `#00d4ff` | Cyan — labels, highlights, acentos secundarios |
| `var(--bg)` | `#0a0a0f` | Fondo principal del body |
| `var(--bg2)` | `#111118` | Fondo secundario |
| `var(--bg3)` | `#1a1a24` | Fondo de cards |
| `var(--border)` | `#2a2a3a` | Bordes de cards |
| `var(--text)` | `#e8e8f0` | Texto principal |
| `var(--text-muted)` | `#8888aa` | Texto secundario / descripción |

**Regla:** nunca usar colores hardcodeados en CSS. Siempre `var(--nombre)`.

## Tipografía
- **Fuente:** `'Segoe UI', system-ui, -apple-system, sans-serif`
- **Tamaños de título:** `clamp(1.6rem, 3vw, 2.2rem)` para section-title
- **Tamaño base:** 1rem (16px)
- **Line-height:** 1.6 para texto corrido

## Espaciado
- **Padding de sección:** `100px 0` desktop · `72px 0` en 768px
- **Gap entre cards:** `24px` estándar
- **Border-radius:** `var(--radius)` = `12px`

## HTML

### Estructura de sección estándar
```html
<section id="nombre-seccion" class="section">
  <div class="container">
    <div class="section-header fade-up">
      <span class="section-label">Etiqueta</span>
      <h2 class="section-title">Título principal</h2>
      <p class="section-desc">Descripción breve opcional.</p>
    </div>
    <!-- contenido -->
  </div>
</section>
```

### Semántica
- Un solo `<h1>` en el hero
- Secciones con `<h2>` como section-title
- Cards internas con `<h3>`
- Usar atributos `aria-label` en elementos interactivos sin texto visible

## CSS

### Convención de comentarios de sección
```css
/* ─── Nombre de la sección ─────────────────────────────── */
```

### Orden de propiedades en regla CSS
1. Display / position / layout
2. Box model (width, height, margin, padding)
3. Tipografía (font, color, text-align)
4. Visual (background, border, border-radius)
5. Efectos (transition, transform, opacity)

### Animaciones
- Duración estándar: `var(--transition)` = `0.3s ease`
- Animaciones de entrada: clase `.fade-up` + `.visible` via Intersection Observer

## JavaScript

### Convenciones de código
- Variables con `const` / `let` — nunca `var`
- Funciones nombradas en camelCase
- Event listeners agrupados por funcionalidad con comentarios
- Canvas: inicializar en función separada por canvas

### Comentarios en JS
```javascript
// ─── Nombre de bloque ───────────────────────────────────
```

## Git

### Commits en español, imperativo
```
Agrego X
Corrijo Y
Actualizo Z
Refactorizo W
```

### Convención de mensajes
- `feat:` o "Agrego" → nueva funcionalidad
- `fix:` o "Corrijo" → corrección de bug
- `copy:` o "Actualizo" → cambios de contenido/texto
- `docs:` → cambios en README o documentación
- `style:` → cambios de CSS sin impacto funcional
