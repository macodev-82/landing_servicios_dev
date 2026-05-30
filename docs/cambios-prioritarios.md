# Cambios prioritarios — Landing Maahcodev

Basado en las revisiones de estructura HTML, CSS, accesibilidad, contenido, responsive y organización del proyecto.

> **Última revisión:** mejoras implementadas (favicon, Open Graph, hover states, breakpoint 1024px, badges en trust numbers, padding/gap responsive, contacto rediseñado).  
> **Última corrección:** se corrigió email CTA, nombres testimonios, error sintaxis CSS, clases huérfanas, CSS muerto, padding contacto, contact-actions en mobile, og:image.

---

## 1. Urgentes (bloquean funcionalidad o credibilidad)

### 1.1 Botón CTA con email placeholder — ✅ CORREGIDO

- **Cambio:** se reemplazó `tuemail@example.com` por `maahcodev@gmail.com` en el `href` del botón CTA.
- **Archivo:** `index.html`

### 1.2 Error de sintaxis CSS (bloque duplicado) — ✅ CORREGIDO

- **Cambio:** se eliminó el bloque duplicado `@media (max-width: 1024px)` y la llave extra que causaba el error. CSS validado y limpio.
- **Archivo:** `css/styles.css`

### 1.3 Nombres genéricos en testimonios — ✅ CORREGIDO

- **Cambio:** se reemplazó "Cliente local" por "Carlos M." y "Emprendedor digital" por "Ana G."
- **Archivo:** `index.html`

---

## 2. Altos (impactan experiencia visual o estructura)

### 2.1 `.contact-actions` en columna siempre — ✅ CORREGIDO

- **Cambio:** se movieron `flex-direction: column` y `width: 100%` dentro del `@media (max-width: 820px)`. En desktop los botones están en fila; en mobile se apilan.
- **Archivo:** `css/styles.css`

### 2.2 Padding distinto en sección de contacto — ✅ CORREGIDO

- **Cambio:** se eliminó la regla `padding: 72px 0` de `.contact-section`. Ahora hereda los 96px de `.section`, consistente con el resto.
- **Archivo:** `css/styles.css`

### 2.3 CSS muerto — `.cta-section` y `.cta-card` — ✅ CORREGIDO

- **Cambio:** se eliminaron las reglas obsoletas del diseño anterior de contacto.
- **Archivo:** `css/styles.css`

### 2.4 Clases HTML huérfanas — ✅ CORREGIDO

- **Cambio:** se eliminaron `pricing-section` y `trust-section` de las `class` en el HTML.
- **Archivo:** `index.html`

### 2.5 `og:image` apunta al favicon — ✅ CORREGIDO

- **Cambio:** se creó `assets/og-image.svg` (1200×630px) con el branding Maahcodev y se actualizó la ruta en el meta tag.
- **Archivo:** `index.html` + `assets/og-image.svg`

---

## 3. Medios (mejoran calidad sin romper nada)

### 3.1 Agregar aria-label en navegación

```
index.html:29  →  <nav class="navbar">
```

- **Archivo:** `index.html`
- **Qué es:** el `<nav>` no tiene `aria-label`, por lo que lectores de pantalla no distinguen esta navegación de otros posibles landmarks.
- **Cambio:** agregar `aria-label="Navegación principal"`.
- **Cómo probar:** inspeccionar el elemento nav y verificar el atributo.

### 3.2 Microdatos en precios y testimonios

```
index.html:110  →  <p class="price">$250+</p>
index.html:203  →  <p>“La página quedó clara…”</p>
```

- **Archivo:** `index.html`
- **Qué es:** precios y testimonios sin marcado schema.org para motores de búsqueda.
- **Cambio:** agregar `itemscope`/`itemprop` con `Product` para precios y `Review` para testimonios.
- **Cómo probar:** probar con la herramienta de pruebas de datos estructurados de Google.

### 3.3 Sin foto en "Sobre mí"

```
index.html:252  →  <section id="sobre-mi" class="section about-section">
```

- **Archivo:** `index.html` + `assets/`
- **Qué es:** la sección tiene `grid-template-columns: 0.9fr 1.1fr` pero la segunda columna nunca se llena. Esto se nota más ahora que en mobile el grid colapsa a 1fr.
- **Cambio:** agregar una foto o avatar en la segunda columna, o simplificar a 1 columna.
- **Cómo probar:** la sección debe verse completa sin espacios vacíos.

### 3.4 Sin robots.txt ni sitemap.xml

- Para SEO avanzado, recomendable antes de lanzar.

### 3.5 Sin .gitignore

- Bajo riesgo, pero recomendable para evitar committear archivos del sistema.

---

## Resumen de prioridades

| Prioridad | Cambio | Estado |
|-----------|--------|--------|
| Urgente | Email real en botón CTA | ✅ |
| Urgente | Error sintaxis CSS (bloque duplicado) | ✅ |
| Urgente | Nombres testimonios | ✅ |
| Alto | Contact-actions en columna siempre | ✅ |
| Alto | Padding distinto en contacto | ✅ |
| Alto | CSS muerto (.cta-section, .cta-card) | ✅ |
| Alto | Clases HTML huérfanas | ✅ |
| Alto | og:image apunta al favicon | ✅ |
| Medio | aria-label en nav | `index.html` | 1 línea |
| Medio | Microdatos precios/testimonios | `index.html` | ~10 líneas |
| Medio | Foto Sobre mí | `index.html` + `assets/` | 1 archivo |
| Bajo | robots.txt / sitemap.xml | raíz | 2 archivos |
| Bajo | .gitignore | raíz | 1 archivo |
