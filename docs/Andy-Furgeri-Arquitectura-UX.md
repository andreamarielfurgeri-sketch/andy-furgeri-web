# ANDY FURGERI
## Arquitectura UX del Sitio
### Documento 02 — Etapa 2: Estructura, Navegación y Flujos de Usuario

---

## INTRODUCCIÓN

Este documento define **la estructura del sitio**, no su diseño visual. Responde tres preguntas antes de dibujar una sola pantalla:

1. ¿Qué páginas necesita el sitio?
2. ¿Qué contenido va en cada una, y en qué orden se lee?
3. ¿Cómo hace el mismo sitio para hablarle bien a un dueño de negocio local (cliente potencial) y a alguien que evalúa contratarte (reclutador/agencia), sin convertirse en dos sitios distintos?

Todo lo que sigue se apoya en las decisiones ya tomadas en el Brand Book: foco principal en negocios y emprendimientos locales, tono sobrio (no vendedor), y portfolio como herramienta también para oportunidades laborales.

---

## 1. OBJETIVOS DE LA ARQUITECTURA

- **Objetivo primario:** que un dueño de negocio local entienda en menos de 10 segundos qué hacés y para quién, y tenga un camino claro para contactarte.
- **Objetivo secundario:** que un reclutador o agencia pueda, sin buscar mucho, encontrar evidencia de criterio estratégico y ejecución real (no solo "trabajé en tal lugar").
- **Objetivo terciario:** dejar la puerta abierta, sin friccionar el mensaje principal, a que una empresa más grande también pueda evaluarte como clienta o como talento.

**Principio de diseño de la arquitectura:** un solo sitio, una sola narrativa — la dualidad cliente/reclutador no se resuelve con secciones separadas tipo "Modo cliente / Modo profesional", sino con una estructura donde el mismo contenido (casos, resultados, criterio) sirve a ambas lecturas. Un caso de éxito con un negocio local es, al mismo tiempo, prueba de venta para un futuro cliente y prueba de seniority para un reclutador.

---

## 2. MAPA DEL SITIO (SITEMAP)

```
Home
├── Servicios
├── Casos / Resultados
├── Sobre mí
├── Recursos (opcional / Etapa posterior)
└── Contacto
```

**Por qué esta estructura y no más páginas:** coherente con el principio de minimalismo del Brand Book — cada página adicional es una decisión que hay que justificar. Cinco páginas (cuatro núcleo + una opcional) alcanzan para cubrir los tres objetivos sin fragmentar la atención del visitante. No se recomienda, en esta etapa, una página de "Precios" pública (ver sección 8) ni un blog obligatorio (ver justificación en sección 3.5).

---

## 3. NAVEGACIÓN PRINCIPAL

**Header (visible en todas las páginas):**

`Logo (isotipo + nombre)` — `Servicios` — `Casos` — `Sobre mí` — `Contacto` (como botón destacado, no como link de texto)

- El botón de Contacto se diferencia visualmente del resto (color de acento) porque es la acción de conversión principal del sitio.
- Navegación fija (sticky) al hacer scroll, pero minimalista — sin sombra dura, con el mismo criterio de "elevación sutil" definido en el sistema visual del Brand Book.
- En mobile: menú hamburguesa simple, sin animaciones complejas de apertura (coherente con "movimiento sutil, nunca juguetón").

**Footer:**

Contacto directo (email, WhatsApp si aplica), redes sociales, isotipo, y un link discreto a una versión de CV/perfil profesional descargable — este último es el guiño silencioso hacia la audiencia de reclutadores, sin ocupar espacio protagónico en el header.

---

## 4. ARQUITECTURA DE CONTENIDO POR PÁGINA

### 4.1 — HOME

La Home tiene un trabajo muy específico: **calificar en 10 segundos** — que el visitante correcto entienda que está en el lugar correcto, y siga bajando.

**Orden de contenido (de arriba hacia abajo):**

1. **Hero:** headline con la propuesta de valor central (ej. variación del eslogan "Estrategia con datos. Marca con criterio.") + una línea de apoyo que aterrice específicamente en negocios locales (ej. "Ayudo a negocios y emprendimientos a conseguir clientes reales a través de redes sociales, con estrategia y datos."). Un solo CTA principal: "Conversemos" o "Quiero potenciar mi negocio" (evitar lenguaje de venta agresiva, coherente con la voz de marca).
2. **Bloque de credibilidad rápida:** 3-4 números o elementos concretos (ej. "+X negocios acompañados", "Meta Ads · Google Ads · Power BI · Estrategia", o logos/rubros de clientes si existen). Esto reemplaza al típico "sobre mí" largo en la Home — la Home no cuenta la historia completa, la insinúa.
3. **Servicios (resumen).** 3 tarjetas minimalistas con los tres servicios reales que se ofrecen, agrupadas por resultado, no por herramienta:
   - **Creación de contenido** — pensado para generar clientes, no solo alcance.
   - **Gestión de campañas** — Meta Ads y Google Ads con foco en resultados medibles.
   - **Branding y diseño de piezas** — para que el negocio se vea profesional y consistente.
   Cada tarjeta lleva a la página de Servicios.
4. **Caso destacado (uno, no un listado):** un mini-caso con resultado concreto y visual (ej. un fragmento de dashboard, una métrica clara). Link a "Ver más casos".
5. **Bloque "Cómo trabajo":** 3 pasos simples (ej. "Diagnóstico → Estrategia → Ejecución y medición") — transmite proceso y seriedad sin ser un manual extenso.
6. **CTA de cierre:** repetición del llamado a la acción principal, con una línea que reduzca fricción (ej. "Una primera conversación no tiene costo ni compromiso").

**Lo que la Home NO debe tener:** biografía completa, listado exhaustivo de todos los servicios con descripción larga, ni un formulario de contacto largo (eso vive en la página de Contacto).

---

### 4.2 — SERVICIOS

**Criterio de organización:** tres servicios reales, presentados en el lenguaje del resultado que le importa al dueño de negocio, no en lenguaje técnico.

**Los tres servicios:**

1. **Creación de contenido para redes sociales** — planificación y producción de contenido pensado para generar clientes, no solo para "estar presente".
2. **Gestión de campañas en redes** — Meta Ads y Google Ads, con foco en conseguir consultas y ventas, no solo alcance o likes.
3. **Branding y diseño de piezas** — identidad visual y anuncios coherentes, para que el negocio se vea profesional.

Cada bloque de servicio incluye: descripción breve (2-3 líneas, sin jerga), para quién es útil (ej. "ideal si ya tenés algo de presencia pero no estás generando clientes"), y un link/CTA a Contacto.

**Nota importante sobre el análisis de datos:** no es un servicio que se ofrezca ni se cobre por separado. Se menciona, si acaso, como parte de "Cómo trabajo" (ver Home) — la lectura de resultados es el criterio con el que se ejecutan los tres servicios de arriba, no un cuarto servicio ni un entregable (dashboard, informe) que el cliente reciba. Esto es clave para no reposicionar la marca como "analista de negocios", algo que se descartó explícitamente.

**Nota importante:** no se recomienda publicar precios fijos en esta página (ver sección 8), pero sí se recomienda dar una idea de "para qué tipo de negocio es esto" para autocalificar al visitante antes de que escriba.

---

### 4.3 — CASOS / RESULTADOS

Esta es la página más importante del sitio en términos de credibilidad, y la que hace el trabajo doble (cliente + reclutador) con más eficacia.

**Estructura de cada caso:**

1. Contexto breve del negocio (rubro, tamaño, zona si es relevante — sin datos sensibles del cliente).
2. El problema/objetivo real (ej. "tenía presencia en redes pero no generaba consultas").
3. Qué se hizo (estrategia + ejecución, en lenguaje simple).
4. Resultado, con un dato concreto — acompañado idealmente de una pieza visual (gráfico simple, captura de dashboard estilizada con el sistema de marca).

**Por qué este formato sirve a ambas audiencias:** un negocio local lee "esto puede pasarme a mí"; un reclutador lee "esta persona piensa en objetivo → estrategia → medición", que es exactamente el criterio que buscaría en un proceso de selección.

**Si todavía no hay casos reales suficientes:** se recomienda no inventar ni exagerar (rompe el valor "integridad profesional" del Brand Book). Alternativas legítimas: casos de proyectos actuales en el rol de Marketing Manager (si se puede compartir sin conflicto de confidencialidad), o un caso "piloto" propio (ej. gestionar la propia marca personal como caso de estudio visible).

---

### 4.4 — SOBRE MÍ

Esta página es donde vive el storytelling completo definido en el Brand Book (Comunicación Social → Marketing Manager → integralidad en construcción).

**Orden de contenido:**

1. Foto personal (siguiendo el estilo fotográfico definido: fondo oscuro/neutro, iluminación de estudio).
2. Historia narrativa breve (el arco ya definido: de la comunicación al dato).
3. Bloque de habilidades/herramientas (Meta Ads, Google Ads, Power BI, etc.) — presentado como capacidades, no como lista de software.
4. Un bloque específico orientado a reclutadores: disponibilidad para roles, tipo de proyectos que busca, y link a CV descargable — sin que este bloque domine visualmente la página (mantiene el foco en negocios locales, pero no esconde la información).

---

### 4.5 — RECURSOS (opcional, no prioritaria para el lanzamiento)

Un blog o sección de contenido educativo (ej. "3 errores comunes al hacer Ads en un negocio local") aporta SEO y refuerza el arquetipo de la Sabia, pero **no es necesaria para el lanzamiento**. Se recomienda dejarla planificada para una segunda fase, para no demorar el sitio principal por contenido que puede construirse después.

---

### 4.6 — CONTACTO

Página simple y de baja fricción:

- Formulario breve: nombre, tipo de negocio/rubro, qué necesita (select simple, no campo abierto largo), y un campo de contacto.
- Alternativa directa: link a WhatsApp o email, para quienes prefieren no llenar formularios (muy relevante para el público de negocios locales, que suele preferir el contacto directo).
- Sin lenguaje de urgencia artificial ("¡Escribime ya!") — coherente con la voz de marca. Una línea simple: "Contame sobre tu negocio y vemos si podemos ayudarte a crecer."

---

## 5. FLUJOS DE USUARIO POR PERSONA

### Flujo — Marina (negocio local)
`Llega por Instagram/recomendación` → `Home (entiende propuesta en 10 seg)` → `Servicios (se autocalifica: "esto es para mí")` → `Casos (ve que funcionó con alguien parecido a ella)` → `Contacto (WhatsApp o formulario)`

### Flujo — Tomás (emprendedor en escalada)
`Llega buscando "cómo invertir en Ads"` → `Home` → `Casos (quiere ver resultados concretos primero)` → `Servicios (entiende el detalle)` → `Contacto`

### Flujo — Valentina (reclutadora/agencia)
`Llega por LinkedIn o referido` → `Sobre mí (directo, buscando trayectoria y criterio)` → `Casos (evalúa forma de pensar y ejecutar)` → `Contacto o descarga de CV`

### Flujo — Empresa grande (oportunista, no buscado activamente)
`Llega por portfolio/referido` → `Casos (evalúa nivel de ejecución)` → `Sobre mí` → `Contacto`

**Lectura clave de estos cuatro flujos:** las páginas de **Casos** y **Sobre mí** son las que más trabajo hacen para las cuatro audiencias. Esto confirma que la inversión de esfuerzo y calidad debe concentrarse ahí, no en agregar más páginas.

---

## 6. PRIORIZACIÓN DE CONTENIDO (QUÉ VA ARRIBA DEL FOLD)

En la Home, por orden de importancia real (no de "lo que da ganas de mostrar primero"):

1. Qué hacés y para quién (headline).
2. Un CTA claro.
3. Evidencia rápida de credibilidad.

Todo lo demás (proceso, servicios en detalle, casos completos) es secundario y puede requerir scroll. Esto es intencional: coherente con el principio de "espacio como lujo" del sistema visual — no se comprime todo arriba para "no hacer scrollear a nadie". El scroll bien guiado es parte de la experiencia premium (igual que en Linear/Framer).

---

## 7. CONSIDERACIONES DE CONVERSIÓN (CTAs)

- Un único CTA principal en todo el sitio: algo equivalente a "Conversemos" — se repite en Home, Servicios y Casos, siempre con la misma etiqueta (consistencia > creatividad en este punto específico).
- Nunca más de un CTA visualmente competido por sección (evita la sensación de "sitio de agencia con botones por todos lados").
- El contacto directo por WhatsApp/email como alternativa al formulario reconoce el comportamiento real del público de negocios locales, que en general prefiere ese canal.

---

## 8. NOTA SOBRE PRECIOS PÚBLICOS

Se recomienda **no publicar precios fijos** en esta etapa. Razones:

- Los servicios (estrategia, gestión de Ads, contenido) varían mucho según tamaño de negocio y alcance — un precio fijo puede des-calificar a un cliente potencial más grande (empresa que quiera contratarte, según lo conversado) antes de que puedas mostrar valor.
- La página de Servicios ya cumple la función de "autocalificación" al describir para qué tipo de negocio es cada servicio, sin necesidad de un número.

Si en el futuro se decide tener paquetes con precio (por ejemplo, para bajar la fricción con negocios muy chicos), se puede evaluar una sección de "Planes" simple — pero no es necesaria para el lanzamiento.

---

## 9. PRÓXIMOS PASOS

Este documento cierra la **Etapa 2: Arquitectura UX**. El siguiente paso es:

**Etapa 3 — Diseño UI:** wireframes de baja fidelidad de cada página definida acá (Home, Servicios, Casos, Sobre mí, Contacto), aplicando la grilla, tipografía, color y sistema visual del Brand Book. Recién después de aprobar wireframes se pasa a diseño visual de alta fidelidad, y solo al final, a código.

---

*Documento elaborado como Arquitectura UX — Andy Furgeri, Marketing Digital para negocios locales.*
