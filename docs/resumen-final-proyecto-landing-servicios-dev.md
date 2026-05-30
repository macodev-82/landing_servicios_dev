# Resumen final del proyecto: Landing Servicios Dev

## 1. Nombre del proyecto

**Landing Servicios Dev**

Ruta local del proyecto:

```bash
~/proyectos_rentables/02_proyectos/landing_servicios_dev
```

Repositorio GitHub:

```text
macodev-82/landing_servicios_dev
```

Demo publicada en GitHub Pages:

```text
https://macodev-82.github.io/landing_servicios_dev/
```

---

## 2. Objetivo del proyecto

El objetivo de este proyecto fue crear una landing page profesional para presentar servicios de desarrollo web de forma clara, moderna y preparada para publicación.

Este proyecto también marcó un cambio importante en la forma de aprender:

> Aprender haciendo y produciendo.

La idea principal fue dejar de crear ejercicios aislados y empezar a construir proyectos reales, publicados y documentados.

---

## 3. Stack utilizado

El proyecto fue construido con una base simple y profesional:

* HTML
* CSS
* Git
* GitHub
* GitHub Pages
* WSL / Ubuntu
* VS Code
* OpenCode
* Antigravity

Se decidió mantener el proyecto en HTML y CSS plano para conservar velocidad, control y simplicidad.

---

## 4. Estructura del proyecto

Estructura principal:

```text
landing_servicios_dev/
├── assets/
│   ├── favicon.svg
│   └── og-image.svg
├── css/
│   └── styles.css
├── docs/
│   ├── cambios-prioritarios.md
│   ├── plan.md
│   └── resumen-final-proyecto-landing-servicios-dev.md
├── .gitignore
├── .nojekyll
├── AGENTS.md
├── index.html
└── README.md
```

---

## 5. Archivos principales

### `index.html`

Archivo principal de la landing page.

Contiene la estructura de la página:

* Header
* Navegación
* Hero
* Trust bar
* Servicios
* Precios
* Confianza y testimonios
* Proceso
* Sobre mí
* Contacto
* Footer

También contiene:

* Metadatos básicos
* Open Graph básico
* Favicon
* Carga de fuentes externas
* SVG inline para iconos

---

### `css/styles.css`

Archivo principal de estilos.

Controla:

* Variables globales
* Colores
* Tipografía
* Espaciados
* Layout
* Hero visual
* Trust bar
* Cards
* Precios
* Testimonios
* Contacto
* Footer
* Responsive design
* Menú hamburger
* Hover states

---

### `assets/favicon.svg`

Icono SVG usado como favicon del sitio.

---

### `assets/og-image.svg`

Imagen SVG preparada para vista previa social / Open Graph.

---

### `docs/plan.md`

Documento de planificación interna del proyecto.

Incluye:

* Objetivo
* Público objetivo
* Secciones principales
* Stack inicial
* Reglas del proyecto
* Mejoras aplicadas
* Próximos pasos posibles

---

### `docs/cambios-prioritarios.md`

Documento usado para organizar mejoras detectadas con OpenCode y análisis visual.

Sirvió para priorizar:

* Tipografía
* Hero visual
* Trust bar
* Menú responsive
* Iconos
* Avatares
* Limpieza CSS
* Mejoras de conversión

---

### `AGENTS.md`

Archivo con reglas para agentes de IA.

Define cómo deben trabajar herramientas como OpenCode dentro del proyecto:

* Explicar antes de modificar.
* Indicar qué archivo se va a tocar.
* Explicar por qué existe ese archivo.
* No borrar secciones sin explicar.
* Mantener HTML semántico.
* Mantener CSS organizado.
* No agregar JavaScript sin aprobación.

---

### `.gitignore`

Archivo para evitar subir archivos innecesarios o sensibles.

Incluye exclusiones para:

* Archivos del sistema
* Configuraciones de editor
* Logs
* Archivos temporales
* Variables de entorno

---

### `.nojekyll`

Archivo agregado para GitHub Pages.

Su objetivo es evitar que GitHub Pages procese el sitio con Jekyll, ya que este proyecto es HTML/CSS plano.

---

## 6. Herramientas usadas durante el proyecto

## WSL / Ubuntu

El proyecto se trabajó dentro de Ubuntu en WSL.

Ruta correcta:

```bash
~/proyectos_rentables/02_proyectos/landing_servicios_dev
```

Regla importante aprendida:

```bash
pwd
```

Antes de usar Git o modificar archivos, siempre se debe confirmar la ubicación actual.

---

## VS Code

VS Code se usó como editor principal.

Comando usado desde WSL:

```bash
code .
```

---

## Git

Git se usó para controlar versiones.

Comandos principales:

```bash
git status
git add .
git commit -m "mensaje del cambio"
git log --oneline
git push
```

Aprendizaje importante:

* Cambios en rojo: modificados, pero no preparados.
* Cambios en verde: preparados para commit.
* `nothing to commit, working tree clean`: todo está guardado.

---

## GitHub

Se creó un repositorio remoto para subir el proyecto.

Remote final:

```text
git@github.com:macodev-82/landing_servicios_dev.git
```

---

## GitHub Pages

Se usó para publicar la landing.

Configuración usada:

```text
Source: Deploy from a branch
Branch: main
Folder: /root
```

Demo final:

```text
https://macodev-82.github.io/landing_servicios_dev/
```

---

## OpenCode

OpenCode se usó como agente de análisis técnico.

Ayudó a revisar:

* HTML
* CSS
* Jerarquía visual
* Responsive design
* Tipografía
* Hero
* Trust bar
* Navegación móvil
* Servicios
* Testimonios

También se instaló la skill:

```text
frontend-design
```

Ubicación detectada:

```bash
/home/maahcodev/.agents/skills/frontend-design/SKILL.md
```

---

## Antigravity

Antigravity se configuró como herramienta de análisis visual y comercial.

Configuración segura usada:

```text
Agent security mode: Strict
Terminal Command Auto Execution: Request Review
Review Policy: Always Ask
Agent Non-Workspace File Access: Off
Agent Auto-Fix Lints: Off
```

Uso acordado:

* Antigravity analiza.
* No modifica automáticamente.
* No ejecuta comandos sin revisión.
* No reemplaza Git, VS Code ni la revisión humana.

---

## 7. Evolución del proyecto

## Versión inicial

Se creó la base de la landing page.

Secciones iniciales:

* Header
* Hero
* Servicios
* Proceso
* Sobre mí
* Contacto
* Footer

Archivos iniciales:

```text
README.md
index.html
css/styles.css
docs/plan.md
assets/
```

---

## Versión 1.1 — Sección de precios

Se agregó una sección de precios con tres paquetes:

* Inicial
* Recomendado
* Avanzado

Cambios principales:

* Nueva sección `#precios`
* Tarjetas de precios
* Paquete recomendado destacado
* Responsive para precios

Archivos modificados:

```text
index.html
css/styles.css
```

---

## Versión 1.2 — Confianza y testimonios

Se agregó una sección para reforzar credibilidad.

Incluye:

* Tres tarjetas de confianza
* Dos testimonios
* Diseño responsive

Archivos modificados:

```text
index.html
css/styles.css
```

---

## Versión 1.3 — Contacto profesional

Se reemplazó la sección de contacto simple por una sección más completa.

Incluye:

* Mensaje de contacto claro
* Botón de email
* Botón para ver paquetes
* Panel con información que el cliente debe enviar
* Email directo

Archivos modificados:

```text
index.html
css/styles.css
```

---

## Versión 1.4 — Mejora visual general

La versión 1.4 fue la fase visual más importante del proyecto.

Incluyó varias mejoras pequeñas y controladas.

---

### 1. Tipografía profesional

Se agregaron fuentes externas:

* Plus Jakarta Sans para títulos.
* DM Sans para textos generales.

Cambios:

* `--font-display`
* `--font-body`
* `body` usa `var(--font-body)`
* `h1`, `h2`, `h3` usan `var(--font-display)`

Archivos modificados:

```text
index.html
css/styles.css
```

---

### 2. Trust bar debajo del hero

Se agregó una barra de confianza después del hero.

Incluye:

* Comunicación clara
* Proceso ordenado
* Base para crecer

Objetivo:

* Reforzar confianza rápidamente.
* Mostrar una forma de trabajo profesional.
* Evitar métricas falsas o logos inventados.

Archivos modificados:

```text
index.html
css/styles.css
```

---

### 3. Menú responsive tipo hamburger

Se agregó un menú móvil sin JavaScript.

Incluye:

* Checkbox oculto
* Label como botón hamburger
* Líneas animadas
* Menú desplegable en móvil

Archivos modificados:

```text
index.html
css/styles.css
```

Nota:

El menú funciona con CSS puro. Más adelante se puede agregar JavaScript ligero si se quiere cerrar automáticamente al hacer clic en un enlace.

---

### 4. Hero visual mejorado

Se mejoró el hero usando CSS.

Cambios:

* Fondo más profundo.
* Gradientes radiales.
* Patrón geométrico sutil.
* Elemento visual decorativo con `::after`.
* Texto protegido con `z-index`.
* Elemento visual oculto en móvil.

Archivo modificado:

```text
css/styles.css
```

---

### 5. Iconos en tarjetas de servicios

Se agregaron iconos SVG inline a las tarjetas de servicios.

Servicios:

* Landing pages
* Sitios web base
* Automatización simple

Objetivo:

* Mejorar escaneo visual.
* Diferenciar servicios.
* Hacer la sección menos textual.

Archivos modificados:

```text
index.html
css/styles.css
```

---

### 6. Avatares en testimonios

Se agregaron avatares con iniciales:

* CM
* AG

Objetivo:

* Dar más presencia visual a los testimonios.
* Evitar usar fotos falsas.
* Mejorar percepción de confianza.

Archivos modificados:

```text
index.html
css/styles.css
```

---

### 7. Espaciado centralizado

Se agregaron variables CSS para controlar espaciados.

Variables:

```css
--spacing-card
--spacing-card-mobile
--spacing-panel
--spacing-feature
```

Objetivo:

* Evitar números sueltos repetidos.
* Mantener consistencia visual.
* Facilitar mantenimiento del CSS.

Archivo modificado:

```text
css/styles.css
```

---

## 8. Publicación del proyecto

El proyecto fue subido a GitHub y publicado con GitHub Pages.

Comandos importantes:

```bash
git remote set-url origin git@github.com:macodev-82/landing_servicios_dev.git
git branch -M main
git push -u origin main
```

También se agregó:

```text
.nojekyll
```

para evitar procesamiento innecesario con Jekyll.

---

## 9. Errores encontrados y aprendizajes

### Error 1: ejecutar comandos Git fuera del proyecto

Ocurrió al ejecutar Git desde:

```bash
/home/maahcodev
```

en vez de:

```bash
/home/maahcodev/proyectos_rentables/02_proyectos/landing_servicios_dev
```

Solución:

```bash
cd ~/proyectos_rentables/02_proyectos/landing_servicios_dev
pwd
git status
```

Aprendizaje:

Antes de usar Git, siempre ejecutar:

```bash
pwd
```

---

### Error 2: remote origin incorrecto

Primero se agregó un remote con placeholder:

```bash
git@github.com:TU_USUARIO/landing_servicios_dev.git
```

Solución:

```bash
git remote set-url origin git@github.com:macodev-82/landing_servicios_dev.git
```

Aprendizaje:

Si `origin` ya existe, no se usa `git remote add` otra vez. Se usa:

```bash
git remote set-url origin URL_CORRECTA
```

---

### Error 3: confusión entre GitHub Account Settings y Repository Settings

Se intentó configurar Pages desde los ajustes generales de la cuenta.

Lugar incorrecto:

```text
Cuenta personal → Settings → Pages
```

Lugar correcto:

```text
Repositorio → Settings → Pages
```

Aprendizaje:

GitHub Pages de un proyecto se activa desde los settings del repositorio, no desde los settings generales de la cuenta.

---

### Error 4: cambios de agentes que requerían revisión

OpenCode hizo propuestas útiles, pero algunos cambios necesitaron ajuste manual.

Ejemplos:

* Trust bar inicialmente demasiado horizontal.
* CSS que requería limpieza.
* Necesidad de revisar HTML y CSS antes de guardar.

Aprendizaje:

Los agentes ayudan, pero no reemplazan la revisión humana.

Flujo correcto:

```text
Agente propone → humano revisa → se prueba → se guarda con Git
```

---

## 10. Flujo profesional definido

Para futuros cambios en este proyecto:

```bash
cd ~/proyectos_rentables/02_proyectos/landing_servicios_dev
pwd
git status
```

Después se editan archivos.

Para probar localmente:

```bash
python3 -m http.server 8000
```

Abrir:

```text
http://localhost:8000
```

Para guardar:

```bash
git diff --check
git status
git add .
git commit -m "mensaje claro"
git push
git status
```

---

## 11. Estado actual

El proyecto actualmente cuenta con:

* Landing page publicada.
* Diseño visual mejorado.
* Hero profesional.
* Trust bar.
* Servicios con iconos.
* Precios.
* Testimonios con avatares.
* Contacto profesional.
* Responsive design.
* Menú hamburger.
* GitHub Pages.
* Documentación base.

Estado:

```text
Proyecto 1 publicado correctamente.
```

---

## 12. Próximas mejoras posibles

### Prioridad alta

1. Crear formulario de contacto real.
2. Agregar sección de proyectos o casos de estudio.
3. Reemplazar el mockup decorativo del hero por un elemento HTML más detallado.

### Prioridad media

1. Agregar `robots.txt`.
2. Agregar `sitemap.xml`.
3. Agregar datos estructurados básicos.
4. Crear una imagen Open Graph más completa.

### Prioridad futura

1. Agregar JavaScript ligero para cerrar el menú mobile al hacer clic.
2. Crear versión avanzada con backend FastAPI.
3. Crear una plantilla reutilizable para clientes.
4. Crear Proyecto 2 con formulario real o una API pequeña.

---

## 13. Conclusión

Este proyecto representa un avance importante porque ya no es solo práctica aislada.

Es un proyecto real:

* Diseñado.
* Versionado con Git.
* Subido a GitHub.
* Publicado con GitHub Pages.
* Mejorado con revisión de agentes.
* Documentado profesionalmente.

El objetivo de “aprender haciendo y produciendo” se cumplió en esta primera fase.

Este proyecto puede servir como:

* Base de portafolio.
* Plantilla para servicios.
* Práctica profesional de HTML/CSS.
* Primer proyecto publicado.
* Punto de partida para proyectos más rentables.
