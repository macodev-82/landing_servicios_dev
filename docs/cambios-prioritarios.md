# Cambios prioritarios — Landing Maahcodev

Basado en las revisiones de estructura HTML, CSS, accesibilidad, contenido, responsive y organización del proyecto.

---

## 1. Urgentes (bloquean funcionalidad o credibilidad)

### 1.1 Reemplazar email placeholder

```
index.html:131  →  href="mailto:tuemail@example.com"
```

- **Archivo:** `index.html`
- **Qué es:** el único medio de contacto funcional apunta a un email de ejemplo
- **Cambio:** reemplazar con el email real del negocio
- **Cómo probar:** abrir el enlace y verificar que abre el cliente de correo con la dirección correcta

### 1.2 Poner nombres reales en testimonios

```
index.html:197  →  <strong>Cliente local</strong>
index.html:208  →  <strong>Emprendedor digital</strong>
```

- **Archivo:** `index.html`
- **Qué es:** los autores de los testimonios son roles genéricos, no nombres
- **Cambio:** usar nombre con inicial (ej: "Carlos M.", "Ana G.") o nombre completo si hay permiso. Esto aumenta la credibilidad sin necesidad de foto real.
- **Cómo probar:** leer la sección Confianza y verificar que los nombres suenan a personas reales

---

## 2. Altos (impactan experiencia visual o navegación)

### 2.1 Unificar padding vertical de secciones

```css
.pricing-section { padding-top: 32px; }   /* style.css:282 */
.trust-section   { padding-top: 32px; }   /* style.css:346 */
```

- **Archivo:** `css/styles.css`
- **Qué es:** `.pricing-section` y `.trust-section` sobreescriben el `padding: 96px 0` de `.section` con `padding-top: 32px`. Resultado: 32px arriba, 96px abajo. Asimetría visual.
- **Cambio:** decidir si las secciones internas usan padding completo (96px) o todas van con `padding-top: 32px`. Lo importante es que sea consistente.
- **Cómo probar:** desplazarse entre Servicios → Precios → Confianza → Proceso. El espaciado superior de cada sección debe verse uniforme.

### 2.2 Diferenciar números de Confianza vs Proceso

```css
.trust-number { font-size: 0.9rem; font-weight: 900; }  /* style.css:369-376 */
.step span    { font-weight: 800; }                      /* style.css:236-241 */
```

- **Archivo:** `css/styles.css`
- **Qué es:** las secciones "Confianza" y "Proceso" usan el mismo patrón de tarjetas numeradas (01, 02, 03) con estilo casi idéntico. El usuario puede pensar que está viendo la misma información dos veces.
- **Cambio:** dar identidad visual distinta a cada una. Por ejemplo: Confianza con iconos o checkmarks en vez de números; o cambiar color, fondo o tamaño para que se diferencien.
- **Cómo probar:** mirar ambas secciones seguidas en navegador y confirmar que se distinguen a simple vista

### 2.3 Agregar breakpoint intermedio para tablets

```css
@media (max-width: 820px) { /* único breakpoint */ }
```

- **Archivo:** `css/styles.css`
- **Qué es:** las cuadrículas de 3 columnas saltan directamente a 1 columna a los 820px. En pantallas de ~900-1024px (tablet vertical) las cards se ven comprimidas.
- **Cambio:** agregar breakpoint `@media (max-width: 1024px)` que pase los grids de 3 a 2 columnas, y mantener el de 820px para 1 columna.
- **Cómo probar:** redimensionar el navegador desde 1200px hasta 400px. Las cards deben reacomodarse suavemente: 3 → 2 → 1 columna.

---

## 3. Medios (mejoran calidad sin romper nada)

### 3.1 Agregar favicon

```
index.html:<head> — sin <link rel="icon">
```

- **Archivo:** `index.html` (y crear `assets/favicon.ico` o `.svg`)
- **Qué es:** no hay icono de pestaña en el navegador
- **Cambio:** agregar `<link rel="icon" href="assets/favicon.svg" type="image/svg+xml">` en el `<head>` y colocar un SVG simple (ej: letra "M" del logo)
- **Cómo probar:** abrir la página y verificar que aparece un icono en la pestaña del navegador

### 3.2 Agregar hover states en cards y price-cards

```
style.css — .card, .price-card, .trust-card, .testimonial-card no tienen hover
```

- **Archivo:** `css/styles.css`
- **Qué es:** las tarjetas son estáticas, solo los botones tienen interacción
- **Cambio:** agregar transición en hover que intensifique la sombra o el borde, siguiendo el patrón existente de los botones
- **Cómo probar:** pasar el mouse sobre cualquier tarjeta y ver un cambio visual sutil

### 3.3 Agregar Open Graph Tags

```
index.html — sin meta tags para redes sociales
```

- **Archivo:** `index.html` `<head>`
- **Qué es:** al compartir el enlace en redes sociales no se muestra vista previa
- **Cambio:** agregar `og:title`, `og:description`, `og:image`, `og:url`. La imagen puede ser un screenshot de la landing o un logo.
- **Cómo probar:** usar el debugger de Facebook o simular el compartido para ver la preview

### 3.4 Agregar microdatos en precios y testimonios

```
index.html:100  →  <p class="price">$250+</p>
index.html:192  →  <p>“La página quedó clara…”</p>
```

- **Archivo:** `index.html`
- **Qué es:** los precios y testimonios no tienen marcado semántico para motores de búsqueda
- **Cambio:** agregar `itemscope`/`itemprop` con schema.org `Product` para precios y `Review` para testimonios
- **Cómo probar:** probar con la herramienta de pruebas de datos estructurados de Google

---

## 4. Bajos (mejoras a futuro, no bloquean)

### 4.1 padding de cards responsive
- `padding: 32px` fijo en price-cards y testimonial-cards. Reducir a `clamp(20px, 4vw, 32px)` en mobile.

### 4.2 gap responsivo
- `gap: 18px` fijo en todos los grids. Agregar `gap: 12px` dentro del media query de 820px.

### 4.3 Sin foto en "Sobre mí"
- La sección tiene `grid-template-columns: 0.9fr 1.1fr` pero la segunda columna está vacía. Agregar una foto o avatar, o simplificar a 1 columna.

### 4.4 Nav sin hamburger menu
- Sin menú responsive en mobile. Requiere JavaScript, por ahora el apilado vertical es aceptable.

### 4.5 Sin robots.txt ni sitemap.xml
- Para SEO avanzado, pero no crítico en etapa inicial.

### 4.6 Sin .gitignore
- Bajo riesgo, pero recomendable para evitar committear archivos del sistema.

---

## Resumen de prioridades

| Prioridad | Cambio | Archivo | Esfuerzo |
|-----------|--------|---------|----------|
| Urgente | Email real | `index.html` | 1 línea |
| Urgente | Nombres testimonios | `index.html` | 2 líneas |
| Alto | Padding consistente | `css/styles.css` | 2 líneas |
| Alto | Diferenciar números | `css/styles.css` | ~5 líneas |
| Alto | Breakpoint tablet | `css/styles.css` | ~8 líneas |
| Medio | Favicon | `index.html` + `assets/` | 1 archivo + 1 línea |
| Medio | Hover cards | `css/styles.css` | ~8 líneas |
| Medio | Open Graph | `index.html` | 4 líneas |
| Medio | Microdatos | `index.html` | ~10 líneas |
| Bajo | Padding/gap resp. | `css/styles.css` | ~4 líneas |
| Bajo | Foto Sobre mí | `index.html` + `assets/` | 1 archivo |
| Bajo | Hamburger menu | Requiere JS | (futuro) |
