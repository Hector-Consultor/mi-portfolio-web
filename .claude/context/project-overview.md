---
created: 2026-03-06T22:51:53Z
last_updated: 2026-03-06T22:51:53Z
version: 1.0
author: Claude Code PM System
---

# Project Overview

## Descripción
Portfolio web de una página para Héctor González, consultor freelance de automatización inteligente. Sitio estático sin dependencias, desplegado en Netlify.

**Live:** https://hgautomation.netlify.app
**Repo:** https://github.com/Hector-Consultor/mi-portfolio-web

## Secciones actuales

| Sección | ID | Estado | Descripción |
|---------|----|--------|-------------|
| Hero | `#hero` | Completo | Canvas de partículas interactivo + presentación |
| Sobre mí | `#sobre-mi` | Completo | Foto, propuesta de valor, 4 diferenciadores |
| Servicios | `#servicios` | Completo | 3 cards: Consultoría, IA Aplicada, Automatización |
| Proyectos | `#proyectos` | Pendiente | Estructura lista, faltan proyectos reales |
| Tecnologías | `#tecnologias` | Completo | Grid con todo el stack de herramientas |
| Contacto | `#contacto` | Completo | Email, WhatsApp, LinkedIn |

## Características implementadas
- Canvas de partículas interactivo con repulsión por mouse
- Mini canvases decorativos en cards de servicios
- Navbar fija con efecto glassmorphism al hacer scroll
- Menú hamburguesa para móvil
- Animaciones fade-up con Intersection Observer
- Stagger animations en grid de tecnologías
- Scrollbar personalizada con color accent
- Smooth scroll entre secciones

## Integraciones
- **GitHub:** repositorio fuente del código
- **Netlify:** hosting y CI/CD automático
- **No hay APIs externas** — el sitio es completamente estático

## Estado de producción
- **Live:** sí
- **CI/CD:** activo (push a main → deploy automático)
- **Errores conocidos:** ninguno
- **Performance:** óptima (sin dependencias externas)
