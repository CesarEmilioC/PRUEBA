# Proyecto — Estrategia Legal (sitio web firma jurídica)

Sitio web estático premium para firma mexicana especializada en **estrategia fiscal, comercio exterior (IMMEX, PROSEC, CIVA), derecho laboral corporativo, auditoría y cumplimiento**. Público objetivo: empresas medianas y grandes del sector manufacturero, exportador y corporativo.

## Stack
HTML5 estático + CSS custom + JS vanilla. Sin build, sin framework. Fuentes vía Google Fonts (Cormorant Garamond serif + Inter sans). Imágenes vía Unsplash (placeholders).

## Estructura
```
/index.html              Home
/firma.html              Sobre la firma
/servicios.html          Overview de servicios
/servicios/              Detalles por área
  estrategia-fiscal.html
  comercio-exterior.html
  derecho-laboral.html
  auditoria-cumplimiento.html
  consultoria-contable.html
/sectores.html  /equipo.html  /insights.html  /contacto.html
/assets/css/styles.css   Design system completo
/assets/js/main.js       Nav, reveal, form
```

## Design system (variables en :root)
- Paleta: `--navy-900 #0a1930` · `--accent #b8935a` (dorado sobrio) · `--gray-50/100/200/500/700/900` · `--white`
- Tipografía: `--font-serif` (títulos) / `--font-sans` (cuerpo)
- Container: 1240px estándar
- Clases base: `.section`, `.section-dark`, `.section-gray`, `.container`, `.btn-primary/secondary/ghost`, `.eyebrow`, `.lead`
- Componentes existentes: `.pillars`, `.services-grid`, `.sectors`, `.split`, `.diff-grid`, `.stats`, `.team-grid`, `.insights-grid`, `.service-detail` (sidebar sticky), `.prose`, `.callout`, `.final-cta`, `.sub-hero`

## Convenciones
- **Todas las páginas replican header/footer inline** (no hay includes). Al editar nav/footer hay que actualizar todas las páginas, o extraer a componente compartido si el cambio es grande.
- Páginas dentro de `/servicios/` usan rutas relativas `../` para assets y navegación.
- Animación scroll reveal con atributo `data-reveal` (IntersectionObserver en main.js).
- Form de contacto en `contacto.html` es placeholder — falta backend real.
- Copy: tono técnico, ejecutivo, sobrio. Evitar "somos los mejores", "excelencia", superlativos genéricos.

## Tareas pendientes probables
- Fotografía corporativa real (reemplazar placeholders Unsplash)
- Logo real de la firma (actualmente marca textual "E" + "Estrategia Legal")
- Datos reales de socios en equipo.html
- Dirección y teléfono reales en contacto.html / footer
- Backend para formulario de contacto
- Páginas individuales de insights (actualmente solo listing)
- Aviso de privacidad y términos
- Favicon

## Notas
- Marca actual "Estrategia Legal" es placeholder — el cliente define el nombre real.
- No hay CMS. Cada publicación de insights requiere editar el HTML.
- Responsive breakpoints: 1024px (tablet) y 768px (mobile).
