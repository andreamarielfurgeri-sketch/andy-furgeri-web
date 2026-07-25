# PROMPT PARA WINDSURF — Sitio Web de Andy Furgeri

> Instrucción de uso: copiar este documento completo como prompt inicial en Windsurf. Contiene toda la identidad de marca, arquitectura y contenido necesarios para construir el sitio de punta a punta. Se puede pegar entero o ir por secciones si Windsurf lo pide en pasos.

---

## CONTEXTO DEL PROYECTO

Quiero que construyas un sitio web de portfolio/marca personal para **Andy Furgeri**, especialista en marketing digital enfocada en ayudar a negocios y emprendimientos locales a conseguir clientes reales a través de redes sociales, con estrategia y datos. El sitio también funciona como portfolio profesional para oportunidades laborales (reclutadores/agencias).

**Referencias de estilo a seguir estrictamente:** Linear.app, Vercel.com, Framer.com, Apple.com. Minimalismo extremo, fondo oscuro dominante, mucho espacio en blanco, animaciones suaves y sutiles, tipografía como protagonista. **NO** debe verse como una landing page de agencia de marketing tradicional (nada de colores saturados, iconos genéricos de "megáfono/gráfico de torta", ni layouts recargados).

---

## STACK TÉCNICO

- **Framework:** Next.js 14+ (App Router)
- **Estilos:** Tailwind CSS
- **Animaciones:** Framer Motion (transiciones sutiles, easing suave, nunca "bounce" ni efectos llamativos)
- **Tipografía:** cargar vía `next/font`
- **Iconos:** Lucide React (línea fina, coherente con la estética)
- **Formulario de contacto:** componente simple, sin backend complejo por ahora (puede simular envío o usar un servicio simple tipo Formspree/Resend — proponé la opción más simple)
- **Responsive:** mobile-first, breakpoints estándar de Tailwind
- **Deploy target:** Vercel

---

## SISTEMA DE MARCA — APLICAR EN TODO EL SITIO

### Paleta de colores (usar como variables CSS / config de Tailwind)

```
--color-bg-deep: #120B36;         /* Índigo profundo — base del degradé */
--color-bg-mid: #241968;          /* Violeta medio — punto medio del degradé */
--color-bg-light: #4B3FA8;        /* Azul-violeta — punto más luminoso del degradé */
--color-surface: rgba(255,255,255,0.07);   /* Fondo de tarjetas (vidrio esmerilado) */
--color-surface-border: rgba(255,255,255,0.16); /* Bordes de tarjetas */
--color-text-secondary: #B8B2DE;  /* Texto secundario, tinte violeta */
--color-text-primary: #F5F5F7;    /* Texto principal */
--color-accent-primary: #A78BFA;  /* Lila — CTAs, hover */
--color-accent-secondary: #6D5FF7;/* Azul violáceo — gráficos, links activos */
--color-accent-deep: #3B4CCA;     /* Azul profundo — detalles, degradés */
--color-glow: #D6C9FF;            /* Lila claro — efectos de luz/glow */
```

**Fondo:** degradé fijo de pantalla completa (`position: fixed`, sin scroll), de `#120B36` a `#241968` a `#4B3FA8`, con un patrón sutil de puntos tipo estrella en baja opacidad superpuesto. El contenido de la página se posiciona por encima de este fondo fijo, nunca lo reemplaza sección por sección.

**Tarjetas y superficies:** todas las tarjetas, bloques y campos de formulario usan `background: var(--color-surface)` + `backdrop-filter: blur(16px)` + `border: 1px solid var(--color-surface-border)` — efecto de vidrio esmerilado, igual al de los widgets nativos de macOS. Nunca usar fondos sólidos opacos para tarjetas en este sistema.

**Regla de uso:** el degradé de fondo ocupa siempre el 100% de la página (no hay secciones con otro color de fondo). Las superficies de vidrio son las que generan la jerarquía visual, no bloques de color sólido. Los acentos lila/azul violáceo se reservan para CTAs, hover states, gráficos y detalles — igual que antes.

### Tipografía

- **Titulares:** General Sans o Söhne (usar la que esté disponible vía Google Fonts/Fontshare; si no, usar una geométrica similar como "Space Grotesk").
- **Cuerpo/UI:** Inter.
- **Acento editorial (opcional, para citas o storytelling en "Sobre mí"):** Fraunces (serif con carácter, usar con moderación).

### Sistema visual

- Grid de 12 columnas, márgenes generosos (mínimo 80-120px en desktop).
- Separación vertical entre secciones: mínimo 96-160px.
- Bordes suavemente redondeados (8-16px) en cards y botones.
- Elevación mediante borde sutil de 1px en gris translúcido + glow leve en violeta en hover, **no** sombras duras tradicionales.
- Transiciones de 200-400ms con easing suave (`ease-out` o curva custom), nunca abruptas.
- Iconografía: solo línea fina (stroke), un color por contexto, sin relleno ni 3D.

---

## TONO DE VOZ (para todos los textos que generes)

- Claro y directo, sin jerga técnica innecesaria.
- Seguro pero cercano — nunca lenguaje de venta agresiva ("¡Contactame YA!", "oferta limitada", exclamaciones excesivas).
- Frases cortas, párrafos breves.
- Primera persona, con seguridad real, sin sobreprometer resultados ("garantizado", "en 30 días") ni subestimarse.

---

## ESTRUCTURA DEL SITIO (SITEMAP)

```
/ (Home)
/servicios
/casos
/sobre-mi
/contacto
```

Header fijo (sticky, sutil) en todas las páginas: Logo — Servicios — Casos — Sobre mí — [Contacto como botón destacado con color de acento].

Footer: contacto directo (email / WhatsApp), redes sociales, link discreto a CV descargable.

---

## CONTENIDO Y ESTRUCTURA POR PÁGINA

### 1. HOME (`/`)

Construir en este orden exacto de secciones:

1. **Hero.** Headline grande (usar variación de: *"Estrategia con datos. Marca con criterio."*) + subheadline: *"Ayudo a negocios y emprendimientos a conseguir clientes reales a través de redes sociales, con estrategia y datos."* + un único CTA: *"Conversemos"* (botón con color de acento, no exclamación).
2. **Bloque de credibilidad rápida.** 3-4 datos/elementos concretos en formato minimalista (ej. herramientas: Meta Ads · Google Ads · Power BI · Estrategia de contenido). Usar tipografía grande, poco texto.
3. **Servicios (resumen).** 3 tarjetas con estos títulos y una línea descriptiva cada una (contenido completo, no placeholder):
   - **Creación de contenido** — Planificación y producción de contenido para redes sociales, pensado para generar clientes, no solo alcance.
   - **Gestión de campañas** — Meta Ads y Google Ads con foco en conseguir consultas y ventas reales.
   - **Branding y diseño de piezas** — Identidad visual y anuncios coherentes con la imagen que tu negocio necesita.
   Cada tarjeta linkea a `/servicios`.
4. **Caso destacado.** Un bloque con un mini-caso (usar contenido placeholder editable: contexto, problema, resultado con dato concreto) + link a "Ver más casos" → `/casos`.
5. **Cómo trabajo.** 3 pasos en formato horizontal/vertical simple: *Diagnóstico → Estrategia → Ejecución y medición.*
6. **CTA de cierre.** Repetir CTA principal con línea de baja fricción: *"Una primera conversación no tiene costo ni compromiso."*

### 2. SERVICIOS (`/servicios`)

Página con las 3 categorías de servicio (mismas que en Home) pero desarrolladas: descripción de 2-3 líneas, "para quién es útil" (ej. "ideal si ya tenés algo de presencia pero no estás generando clientes"), y CTA a `/contacto` en cada bloque. **No incluir precios fijos. No incluir análisis de datos ni Power BI como servicio ofrecido** — esa habilidad se menciona solo en `/sobre-mi` como parte de cómo trabaja, nunca como un servicio que se contrata por separado.

### 3. CASOS (`/casos`)

Grid o lista de casos. Cada caso con esta estructura (crear 2-3 casos con contenido placeholder realista y editable, marcados claramente como `[EDITAR: contenido real del caso]`):

1. Contexto breve del negocio (rubro, tamaño, zona).
2. Objetivo/problema real.
3. Qué se hizo.
4. Resultado con dato concreto, acompañado de un elemento visual simple (gráfico de barras o línea minimalista con Framer Motion/SVG, usando la paleta de acento).

### 4. SOBRE MÍ (`/sobre-mi`)

1. Foto personal (placeholder de imagen, dejar espacio para reemplazar).
2. Storytelling narrativo (usar este texto como base, se puede ajustar el copy exacto):
   > "Estudié Comunicación Social porque siempre me interesó entender cómo se construye un mensaje. Con el tiempo empecé a moverme hacia el análisis: campañas, métricas, dashboards, Power BI. Hoy trabajo combinando las dos cosas — la sensibilidad de la comunicación y el criterio de los datos — ayudando a negocios locales a conseguir clientes reales. Mi próximo paso es sumar UX/UI."
3. Bloque de habilidades/herramientas (Meta Ads, Google Ads, Power BI, Análisis de datos, Branding, Automatización con IA) en formato de tags/chips minimalistas.
4. Bloque orientado a reclutadores (más discreto visualmente): disponibilidad para roles, tipo de proyectos que busca, botón "Descargar CV".

### 5. CONTACTO (`/contacto`)

- Formulario simple: nombre, tipo de negocio/rubro (select), qué necesita (select: Conseguir clientes / Analizar mis datos / Branding / Otro), email o teléfono.
- Alternativa visible: botón directo a WhatsApp y email.
- Copy de apoyo: *"Contame sobre tu negocio y vemos si podemos ayudarte a crecer."* (sin urgencia artificial).

---

## COMPORTAMIENTO Y ANIMACIONES

- Fade-in + leve desplazamiento vertical (16-24px) al entrar elementos en viewport (usar `whileInView` de Framer Motion), con `once: true` para no repetir en cada scroll.
- Hover en botones: leve glow en color de acento + escala mínima (1.02), transición suave.
- Sin animaciones tipo "typewriter", sin parallax exagerado, sin efectos de scroll "juguetones".
- Header con transición sutil de fondo (de transparente a `bg-secondary` con blur) al hacer scroll.

---

## ACCESIBILIDAD Y BUENAS PRÁCTICAS

- Contraste de texto AA mínimo sobre fondo oscuro (verificar que `#8A8A9A` sobre `#0A0A0F` cumpla, ajustar si hace falta).
- Etiquetas semánticas correctas (`<nav>`, `<main>`, `<footer>`, headings en orden jerárquico).
- Formulario de contacto con labels accesibles, no solo placeholders.
- Meta tags de SEO básico por página (title, description) — relevante porque el público objetivo busca "marketing digital para negocios locales" y variantes.
- Imágenes con `alt` descriptivo.

---

## ENTREGABLE ESPERADO

1. Proyecto Next.js funcional con las 5 rutas definidas.
2. Componentes reutilizables (Header, Footer, Button, Card, CTASection) en carpeta `/components`.
3. Configuración de Tailwind con la paleta y tipografía de marca ya cargadas en `tailwind.config`.
4. Contenido real de este documento ya insertado (no lorem ipsum), con los casos marcados claramente como editables.
5. Responsive completo (mobile, tablet, desktop).

Empezá por el layout base (Header + Footer + configuración de Tailwind/fuentes), después la Home, y luego el resto de las páginas en el orden en que aparecen en el sitemap.
