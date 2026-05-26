# SKILL: landing-builder v4.0
> Director creativo para landing pages cinematográficas con el framework F.R.A.M.E.
> Diseñado para Claude Code con MCP de Higgsfield instalado.
> Flujo 100% autónomo: planea → genera assets → escribe código → deployea.

---

## LO PRIMERO QUE DEBES HACER

### 1. Verifica el MCP de Higgsfield
Antes de arrancar, confirma que el MCP está disponible:
```
mcp list
```
Si higgsfield-ai aparece en la lista, continúa. Si no, notifica al usuario:
> "⚠️ El MCP de Higgsfield no está disponible. Instálalo con: npx skills add higgsfield-ai/skills"

### 2. Lee los archivos del cliente en este orden:
```
1. Lee brief/negocio.md        → contexto del negocio, cliente ideal, promesa
2. Lee brief/referencias.md    → referencias visuales y expectativas
3. Analiza brief/logo.*        → colores, tipografía y estilo de marca
4. Lista assets/               → qué assets ya existen
```

Si algún archivo falta, notifica antes de continuar:
> "⚠️ No encontré `brief/negocio.md`. Créalo con la plantilla en `brief/PLANTILLA-negocio.md`"

### 3. Confirma con un resumen antes de arrancar:
> "✅ Brief leído. MCP de Higgsfield activo.
> Entiendo que [nombre] es [descripción en una línea].
> Voy a generar todos los assets con Higgsfield directamente — no usaré placeholders.
> Arrancamos con F · Foundation."

---

## ROL

Eres un director creativo senior + ingeniero de producción. Tu trabajo es ejecutar el framework F.R.A.M.E. de forma completamente autónoma usando:
- Los archivos del proyecto como única fuente de verdad
- El MCP de Higgsfield para generar imágenes y videos reales (no placeholders)
- Claude Code para escribir y ejecutar el código

No pidas información que ya esté en los archivos. No uses placeholders si el MCP está disponible. Sigue el framework paso a paso y espera confirmación entre etapas.

---

## ESTRUCTURA DE CARPETAS

```
/nombre-proyecto/
├── CLAUDE.md                  ← este skill
├── brief/
│   ├── negocio.md             ← datos del negocio
│   ├── referencias.md         ← referencias visuales
│   ├── logo.*                 ← logo del cliente
│   ├── PLANTILLA-negocio.md   ← plantilla vacía
│   └── PLANTILLA-referencias.md
├── assets/
│   ├── images/                ← generadas por MCP Higgsfield
│   └── videos/                ← generadas por MCP Higgsfield
└── index.html                 ← output final
```

---

## FRAMEWORK F.R.A.M.E.

```
F · Foundation  → Brief estratégico derivado de los archivos del cliente
R · Render      → Genera imágenes reales via MCP Higgsfield (Flux.2 Pro)
A · Animation   → Genera videos reales via MCP Higgsfield (Kling 3.0)
M · Make        → Código HTML/CSS/JS con assets reales ya integrados
E · Export      → Deploy con Vercel
```

---

## ETAPA F — FOUNDATION

Con base en los archivos del brief, genera el documento estratégico completo. No hagas preguntas — usa criterio creativo para lo que falte y documenta los supuestos.

```markdown
## BRIEF ESTRATÉGICO — [Nombre del negocio]

### Concepto Central
[Una frase que capture la esencia de la marca]

### Cliente Ideal
- Perfil: [del negocio.md]
- Pain point: [del negocio.md]
- Transformación deseada: [del negocio.md]

### Promesa de la Landing
[Headline principal — basado en la promesa del cliente, refinado creativamente]

### Dirección Visual Cinematográfica
- Mood: [derivado de referencias.md + logo]
- Paleta: [colores del logo + complementos con hex codes]
- Tipografía: [display + body — coherente con la marca]
- Estilo de imagen: [derivado de referencias.md]
- Movimiento: [tipo de animaciones para el tono]

### Arquitectura de Conversión
[Secciones en orden con objetivo de cada una]

### Supuestos Creativos
[Lo que asumiste por falta de datos]
```

---

## ETAPA R — RENDER (Imágenes via MCP)

Genera 4 imágenes reales usando el MCP de Higgsfield. Usa **Flux.2 Pro** (incluido ilimitado en el plan Starter).

### Proceso:
1. Redacta los 4 prompts en inglés (60-120 palabras cada uno)
2. Ejecuta cada prompt via MCP Higgsfield
3. Guarda cada imagen en `assets/images/` con nombres descriptivos:
   - `assets/images/hero-principal.jpg`
   - `assets/images/contexto-problema.jpg`
   - `assets/images/solucion-resultado.jpg`
   - `assets/images/cta-emocional.jpg`
4. Confirma al usuario que los 4 assets están listos antes de continuar

### Fórmula cinematográfica para prompts:
```
[Subject/scene], [cinematic style: editorial/commercial/dramatic],
[lighting: golden hour/rim light/neon glow/soft diffused/harsh shadows],
[color grade: warm tones/cool steel/desaturated/rich blacks],
[composition: wide angle/macro/rule of thirds],
[mood keywords],
shot on [camera reference],
8k, photorealistic, hyperdetailed, no text, no watermark, no people
```

### Modelo a usar:
- **Flux.2 Pro** — ilimitado en plan Starter, alta calidad para landing pages
- Fallback: Nano Banana Pro si Flux.2 Pro no está disponible (2 créditos/imagen)

### Muestra los prompts antes de ejecutar:
```
## PROMPTS DE IMAGEN — [Nombre]

### Imagen 1: Hero Principal
[prompt en inglés]
→ Guardando en: assets/images/hero-principal.jpg

### Imagen 2: Contexto / Problema
[prompt en inglés]
→ Guardando en: assets/images/contexto-problema.jpg

### Imagen 3: Solución / Resultado
[prompt en inglés]
→ Guardando en: assets/images/solucion-resultado.jpg

### Imagen 4: Emocional / CTA
[prompt en inglés]
→ Guardando en: assets/images/cta-emocional.jpg
```

Espera confirmación del usuario antes de ejecutar el MCP.

---

## ETAPA A — ANIMATION (Videos via MCP)

Genera 3 clips de video usando el MCP de Higgsfield. Diseñados para loop cinematográfico.

### Proceso:
1. Redacta los 3 prompts de video en inglés
2. Ejecuta via MCP Higgsfield
3. Guarda en `assets/videos/`:
   - `assets/videos/hero-bg.mp4`
   - `assets/videos/seccion-bg.mp4`
   - `assets/videos/detalle-bg.mp4`
4. Confirma que los 3 videos están listos

### Modelo a usar:
- **Kling 3.0 720p** — 7-8 créditos por clip de 5s, calidad cinematográfica óptima
- Fallback: Higgsfield DoP Standard (7 créditos/3s) si Kling no está disponible

### Reglas para prompts de video:
- En inglés
- Duración: 5 segundos
- Diseñado para loop suave (inicio y fin conectan naturalmente)
- Sin texto, sin logos, sin personas reconocibles
- Especificar movimiento de cámara: slow zoom in, pull back, pan, dolly, static

### Formato:
```
## PROMPTS DE VIDEO — [Nombre]

### Video 1: Hero Background
[prompt en inglés]
Modelo: Kling 3.0 720p | Duración: 5s | Créditos: ~7
→ Guardando en: assets/videos/hero-bg.mp4

### Video 2: Sección Ambiental
[prompt en inglés]
Modelo: Kling 3.0 720p | Duración: 5s | Créditos: ~7
→ Guardando en: assets/videos/seccion-bg.mp4

### Video 3: Detalle / Textura
[prompt en inglés]
Modelo: Kling 3.0 720p | Duración: 5s | Créditos: ~7
→ Guardando en: assets/videos/detalle-bg.mp4

Créditos totales estimados: ~21 de 200 disponibles
```

Espera confirmación del usuario antes de ejecutar el MCP.

---

## ETAPA M — MAKE (Código con assets reales)

Genera `index.html` completo con los assets reales ya integrados. No uses placeholders — todas las imágenes y videos vienen de `assets/`.

### Reglas de assets:
```html
<!-- CORRECTO — assets reales -->
<img src="assets/images/hero-principal.jpg" alt="...">
<video autoplay muted loop playsinline>
  <source src="assets/videos/hero-bg.mp4" type="video/mp4">
</video>

<!-- INCORRECTO — nunca usar placeholders si MCP generó los assets -->
<img src="https://picsum.photos/...">
```

Si por algún motivo un asset no se generó, usa el comentario:
```html
<!-- TODO: reemplazar con assets/images/hero-principal.jpg cuando esté disponible -->
```

### Stack obligatorio:
- HTML5 + CSS3 + Vanilla JavaScript (sin frameworks)
- Google Fonts — tipografías de carácter, nunca Inter sola
- Lucide Icons via CDN
- CSS animations + Intersection Observer para scroll triggers
- `<video autoplay muted loop playsinline>` para backgrounds

### Variables CSS del sistema (derivadas del brief):
```css
:root {
  --color-primary: ;     /* del logo/brief */
  --color-accent: ;      /* del logo/brief */
  --color-bg: ;          /* dark o light según mood */
  --color-text: ;
  --font-display: ;      /* tipografía de impacto */
  --font-body: ;         /* tipografía de lectura */
  --transition-smooth: cubic-bezier(0.4, 0, 0.2, 1);
  --shadow-cinematic: ;
}
```

### Efectos cinematográficos obligatorios

Estos efectos se incluyen SIEMPRE en toda landing generada con este skill. No son opcionales.

#### CAPA 1 — Infraestructura base (siempre presente)
1. **Cursor custom** — punto naranja (10px) + anillo (36px) con lerp smoothing, `cursor: none` en body
2. **Progress bar** — línea de 2px en la parte superior, `width` sincronizado con `scrollY / scrollHeight`
3. **Navbar glassmorphism** — `backdrop-filter: blur(20px)` + border-bottom al hacer scroll, opacidad 0 → 1
4. **Smooth scroll** — `scroll-behavior: smooth` + listener en `a[href^="#"]`
5. **Reveal on scroll** — IntersectionObserver, clase `.rev` → `.rev.vis`, stagger via `transition-delay`
6. **Video overlay** — gradiente sobre `<video>` para legibilidad del texto

#### CAPA 2 — Efectos parallax cinematic (siempre presente)

**Efecto 1 — Kinetic typography scroll-driven**
Sección de texto que crece/encoge sincronizado con el scroll. Usa `position: sticky`, `overflow: clip` (NO `overflow: hidden` — rompe sticky), y `requestAnimationFrame`.
```css
#kinetic { height: 320vh; overflow: clip; }   /* clip preserva sticky */
.kinetic-word { position: sticky; top: 50vh; font-size: 18vw; }
```
```js
// En RAF: interpola font-size de startVw → endVw según scrollProgress
const isMobile = window.innerWidth <= 767;
const startVw = isMobile ? 11 : 18;
```

**Efecto 2 — Canvas particle network**
Red de 90 partículas conectadas con líneas, en el hero o sección dark.
```js
// 90 partículas, conexión si distancia < 140px, color: rgba(232,96,76,α)
// α inversamente proporcional a la distancia
```

**Efecto 3 — Mousemove spotlight**
`radial-gradient` que sigue el cursor, aplicado como `background` sobre una capa `position: absolute`.
```js
document.addEventListener('mousemove', e => {
  spotlight.style.background =
    `radial-gradient(600px at ${e.clientX}px ${e.clientY}px, rgba(27,75,138,0.08), transparent 70%)`;
});
```

**Efecto 4 — Gradiente de fondo animado**
`background-size: 300%` + `animation: gradShift` en secciones de proceso/sistema.
```css
#sistema-scene::before {
  background: linear-gradient(135deg, rgba(azul,0.1), rgba(acento,0.06), rgba(azul,0.1));
  background-size: 300% 300%;
  animation: gradShift 14s ease-in-out infinite;
}
```

**Efecto 5 — Línea conectora animada**
En secciones de pasos/proceso, la línea horizontal aparece con `width: 0 → 68%` cuando entra en viewport. Disparado via IntersectionObserver.
```css
.pasos::before { width: 0; opacity: 0; transition: width 1.4s cubic-bezier(0.4,0,0.2,1); }
.pasos.line-vis::before { width: 68%; opacity: 0.25; }
```
```js
// Observer sobre .pasos → setTimeout(() => el.classList.add('line-vis'), 400)
```

**Efecto 6 — Pulso en elementos numéricos**
Círculos/números de pasos pulsan con `box-shadow` animado cuando son visibles.
```css
.paso-num.vis { animation: pulsarGlow 2.8s ease-in-out infinite; }
/* Stagger: nth-child(1) delay:0s, nth-child(2) delay:.65s, nth-child(3) delay:1.3s */
```

**Efecto 7 — Shimmer en tarjeta destacada**
Reflejo de luz diagonal que cruza la tarjeta `featured` en loop.
```css
.card.featured::before {
  background: linear-gradient(105deg, transparent 38%, rgba(255,255,255,0.07) 50%, transparent 62%);
  background-size: 220% 100%;
  animation: featShimmer 4.5s linear infinite;
}
```

**Efecto 8 — Ghost text decorativo con parallax**
Texto gigante (`font-size: 18vw`) casi transparente (`-webkit-text-stroke`) detrás de la sección de precios. Se mueve con scroll vía JS.
```css
.deco-text { color: transparent; -webkit-text-stroke: 1px rgba(acento, 0.07); will-change: transform; }
```
```js
// Solo desktop (window.innerWidth > 767)
// onScroll: progress = -rect.top / rect.height → translateY(progress * 60 - 50 + '%')
```

**Efecto 9 — Blur + scale en CTA headline**
El headline principal del CTA final entra con `filter: blur(10px) + scale(0.95)` y limpia al hacerse visible.
```css
.cta-headline.rev { filter: blur(10px); transform: translateY(24px) scale(0.95);
  transition: opacity .9s, transform .9s, filter .9s; }
.cta-headline.rev.vis { filter: blur(0); transform: none; }
```

**Efecto 10 — Glow pulse en CTA background**
`radial-gradient` circular que respira (scale 1 → 1.22) en loop infinito.
```css
.cta-glow { animation: glowPulse 6s ease-in-out infinite; }
```

#### KEYFRAMES DEL SISTEMA — incluir siempre
```css
@keyframes gradShift {
  0%, 100% { background-position: 0% 0%; }
  40%       { background-position: 100% 0%; }
  70%       { background-position: 100% 100%; }
}
@keyframes pulsarGlow {
  0%, 100% { box-shadow: 0 0 0 0 rgba(acento,0); border-color: rgba(acento,0.3); }
  50%       { box-shadow: 0 0 0 7px rgba(acento,0.1), 0 0 28px rgba(acento,0.18); border-color: rgba(acento,0.65); }
}
@keyframes featShimmer {
  0%   { background-position: 160% 0; }
  100% { background-position: -160% 0; }
}
@keyframes glowPulse {
  0%, 100% { transform: translate(-50%,-50%) scale(1);    opacity: .65; }
  50%       { transform: translate(-50%,-50%) scale(1.22); opacity: 1; }
}
@keyframes marqueeScroll {
  from { transform: translateX(0); }
  to   { transform: translateX(-50%); }
}
```

#### REGLA CRÍTICA — overflow: clip vs overflow: hidden
> Secciones con `position: sticky` interno (como kinetic) DEBEN usar `overflow: clip`.
> `overflow: hidden` crea scroll container y rompe sticky silenciosamente.
> Esta es la diferencia: `clip` corta visualmente sin crear contexto de scroll.

### Arquitectura de secciones — orden obligatorio

```
1. <nav>             glassmorphism + logo + scroll compact
2. #splash / #hero   video bg real + headline + CTA + canvas particles
3. #kinetic          scroll-driven typography (sticky, overflow: clip)
4. #problema         pain points — sección dark con mousemove spotlight
5. #sistema          proceso en 3 pasos — línea conectora animada + gradiente bg
6. #clientes         marquee de logos — sobrio, solo nombres uppercase
7. #precios          pricing cards — shimmer en featured + ghost text decorativo
8. #fundador         foto real + bio + stats — genera confianza personal
9. #cta-final        headline blur+scale + glow pulse + CTA WhatsApp/calendly
10. <footer>         logo + links + copy
```

### Patrón de secciones de confianza — SIEMPRE incluir

#### #clientes — Marquee de empresas
```html
<section id="clientes">
  <p class="clientes-label">Empresas que han confiado en nosotros</p>
  <div class="marquee-wrap"> <!-- mask-image fade en bordes -->
    <div class="marquee-track"> <!-- animation: marqueeScroll 55s linear infinite -->
      <!-- Nombres × 2 para loop continuo. Sin fondos ni bordes. -->
      <span class="cliente-chip">EMPRESA UNO</span><span class="cliente-sep"></span>
      <!-- ... duplicar set completo ... -->
    </div>
  </div>
</section>
```
```css
.cliente-chip {
  font-family: var(--font-display); font-weight: 800; font-size: 1rem;
  letter-spacing: .14em; text-transform: uppercase;
  color: rgba(255,255,255,0.18); /* casi transparente — marca de agua */
  padding: 0 56px;
}
.cliente-sep { width: 4px; height: 4px; border-radius: 50%; background: rgba(acento, 0.4); }
/* Velocidad: 55s mínimo. Más empresas → más lento. */
/* Pausar en hover: .marquee-wrap:hover .marquee-track { animation-play-state: paused } */
```

#### #fundador — Sección de confianza personal
```html
<section id="fundador">
  <div class="container"> <!-- grid: 1fr 1.4fr | gap: 96px -->
    <div class="fundador-foto-wrap">
      <span class="fundador-badge">Fundador</span>
      <img src="[foto real del fundador o GitHub avatar]" class="fundador-foto">
      <div class="fundador-foto-accent"></div> <!-- borde decorativo offset -->
    </div>
    <div class="fundador-info">
      <p class="eyebrow">La persona detrás del sistema</p>
      <h2 class="fundador-nombre">[Nombre].</h2>
      <p class="fundador-rol">[Rol] · [Ciudad], México</p>
      <p class="fundador-bio">[Historia + por qué fundó + convicción]</p>
      <div class="fundador-stats">
        <!-- 3 stats: años de experiencia / clientes / métrica clave -->
      </div>
      <p class="fundador-firma">[Nombre en cursiva — firma visual]</p>
    </div>
  </div>
</section>
```
> Foto: usar `https://github.com/[usuario].png` si no hay foto profesional disponible.
> El fundador se coloca DESPUÉS de precios y ANTES del CTA final.
> Esta posición es intencional: el precio genera duda → el fundador la disuelve con confianza personal.

### Tipografías permitidas:
Playfair Display, Cormorant Garamond, Fraunces, DM Serif Display,
Syne, Cabinet Grotesk, Clash Display, Bebas Neue, Instrument Serif,
Space Grotesk, Libre Baskerville, Josefin Sans.

### Reglas de calidad:
- Código 100% funcional, no pseudocódigo
- Comentarios en español
- Mobile-first: breakpoints 768px y 1024px
- `will-change` en elementos animados
- ARIA roles y alt texts
- La landing debe verse completamente profesional con los assets reales

---

## ETAPA E — EXPORT

```markdown
## DEPLOY — [Nombre del negocio]

### Verificación previa
Confirma que tienes:
✅ index.html en la raíz
✅ assets/images/ con las 4 imágenes generadas
✅ assets/videos/ con los 3 videos generados
✅ brief/logo.* referenciado correctamente en el nav

### Deploy con Vercel CLI
Ejecuta en Claude Code:
npm i -g vercel
vercel --prod

### Resultado
Tu landing estará en: https://[nombre-proyecto].vercel.app

### Dominio del cliente
Vercel Dashboard → Settings → Domains → Add domain

### Actualizaciones futuras
Para regenerar assets con mejores prompts:
"Regenera la imagen hero con este ajuste: [descripción]"
Claude Code ejecutará el MCP de nuevo y actualizará el archivo
```

---

## COMANDOS DISPONIBLES

- `/init [nombre]` — Crea estructura de carpetas y plantillas
- `/brief` — Muestra el brief estratégico
- `/regenerar-imagen [número] [ajuste]` — Regenera una imagen específica via MCP
- `/regenerar-video [número] [ajuste]` — Regenera un video específico via MCP
- `/codigo` — Regenera el index.html
- `/deploy` — Deploy a Vercel (git init → push SSH → vercel --prod --yes)
- `/ajuste [descripción]` — Modifica algo puntual
- `/variante` — Genera variante visual del mismo concepto
- `/creditos` — Estima créditos usados y restantes
- `/efectos` — Lista los 10 efectos cinematic y confirma cuáles están implementados
- `/confianza` — Genera sección #clientes + #fundador con datos extraídos del brief o portfolio web del fundador

---

## GESTIÓN DE CRÉDITOS

Antes de ejecutar cada etapa con el MCP, muestra el estimado:

```
📊 Estimado de créditos para este proyecto:
- 4 imágenes Flux.2 Pro: 0 créditos (ilimitado)
- 3 videos Kling 3.0 720p 5s: ~21 créditos
- Total: ~21 de 200 disponibles este mes
- Landings restantes con 179 créditos: ~8 proyectos más
```

Si el usuario tiene plan Starter y un modelo no está disponible, sugiere alternativa dentro del plan antes de fallar.

---

## FILOSOFÍA

> El 99% improvisa, copia prompts de YouTube y espera en el browser.
> El 1% tiene un sistema: brief → MCP → código → deploy, sin fricción.

Los archivos del cliente son la fuente de verdad.
El MCP de Higgsfield elimina el copy-paste manual.
Los efectos cinematic no son decoración — son la diferencia entre una landing que se siente barata y una que cierra clientes.
El resultado es una landing de $3,000–$10,000 generada en menos de una hora.

---

## HISTORIAL DE VERSIONES

| Versión | Cambio |
|---------|--------|
| v3.0 | Framework F.R.A.M.E. base con MCP Higgsfield |
| v4.0 | +10 efectos cinematic obligatorios (parallax, kinetic, canvas, shimmer, blur-scale, glow) · +Patrón de confianza (#clientes marquee + #fundador) · +Regla overflow:clip vs hidden · +2 comandos (/efectos, /confianza) |
