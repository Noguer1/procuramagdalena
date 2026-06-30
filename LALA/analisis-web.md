# Análisis web — Escudero Nocea · Procuradora de los Tribunales

> Objetivo: maximizar captación de clientes (particulares y despachos de abogados)

---

## 1. Qué tiene la web actualmente

### Estructura de secciones

| # | Sección | ID | Público objetivo |
|---|---------|-----|-----------------|
| 1 | **Hero** | `#hero` | General |
| 2 | **Selector de audiencia** | `#audiencia` | Bifurcación particular / despacho |
| 3 | **Sobre mí** | `#sobre` | General |
| 4 | **Qué hago (tabs)** | `#que-hago` | Particulares |
| 5 | **Para despachos** | `#despachos` | Despachos de abogados |
| 6 | **Testimonios** | `#testimonios` | General |
| 7 | **FAQ** | `#faq` | General |
| 8 | **Contacto** | `#contacto` | General |
| 9 | **Footer** | — | — |

### Contenido por sección

**Hero**
- Nombre completo y título profesional
- Credenciales: Nº colegiada 337, desde 1994, Sevilla
- CTA doble: "Solicitar consulta" + "Conocer más"
- 4 stats: 30+ años, año 1994, Nº 337, Sevilla
- Foto de la procuradora (columna derecha, oculta en móvil)

**Audiencia**
- Tarjeta "Particular" → enlaza a `#que-hago`
- Tarjeta "Despacho de abogados" → enlaza a `#despachos`
- Mecanismo de segmentación inteligente que dirige a cada tipo de cliente a su contenido relevante

**Sobre mí**
- Texto biográfico (3 párrafos)
- Stats laterales: 30+ años, 6 jurisdicciones, Nº 337
- Credencial strip: colegio, nº, identificador único, ámbito

**Qué hago (tabs)**
- Tab 1 — Áreas de actuación (6 jurisdicciones):
  - Civil, Penal, Familia, Contencioso-Administrativo, Social, Mercantil e Insolvencia
- Tab 2 — Cómo trabajamos (4 pasos):
  - Primera consulta → Estrategia procesal → Actuación y seguimiento → Resolución y ejecución

**Para despachos**
- Propuesta de valor B2B diferenciada
- 3 pilares: Respuesta 24h · Transparencia total · Toda la jurisdicción
- CTA WhatsApp directo preconfigurado con mensaje personalizado
- CTA secundario al formulario

**Testimonios**
- 3 testimonios de letrados/despachos con nombre, cargo, despacho y años de colaboración
- Rafael Domínguez (12 años) · Ana Belén Fuentes (8 años) · Javier Carmona (10 años)

**FAQ**
- 6 preguntas:
  1. Diferencia abogado/procurador
  2. Cuándo es obligatorio el procurador
  3. Honorarios y tabla de aranceles (con tramos por cuantía)
  4. Cómo colaborar (pasos B2B)
  5. Ámbito geográfico (Sevilla + colaboradores nacionales)
  6. Cambio de procurador a mitad de procedimiento

**Contacto**
- Dirección: Evangelista 7, Bl.F-1, 2º-2 · 41010 Sevilla
- Teléfonos: 625 461 289 · 954 334 651
- Email: magdalenaescudero@hotmail.com
- Horario: L–V 09:00–14:00 / 16:00–19:00
- Formulario: nombre, apellidos, email, teléfono, jurisdicción (select), mensaje

**Elementos flotantes / globales**
- Botón WhatsApp flotante (fijo, abajo derecha) con mensaje preescrito para particulares
- Cursor personalizado (puntero estilizado en dorado)
- Loader animado al cargar
- Navegación fija con scroll-effect (fondo semi-transparente al bajar)
- Menú móvil overlay

### Aspectos técnicos destacables
- HTML/CSS/JS puro, sin frameworks
- Diseño: paleta borgoña + champán, tipografía editorial (Playfair Display + Jost)
- Animaciones de entrada con IntersectionObserver
- Responsive (breakpoints 640px y 900px)
- Metadatos SEO básicos (title + description)
- Cursor personalizado desactivado en dispositivos táctiles

---

## 2. Puntos fuertes para la captación de clientes

- **Bifurcación de audiencia temprana**: el selector particular/despacho encamina al visitante hacia contenido relevante desde el principio, reduciendo fricción.
- **Credenciales numéricas visibles**: 30 años, Nº 337, 1994 — generan confianza inmediata sin necesidad de leer texto largo.
- **WhatsApp preconfigurado**: reduce la barrera de contacto al mínimo, especialmente para despachos B2B.
- **FAQ con tabla de aranceles**: elimina la opacidad de precios, que es una fricción habitual en servicios jurídicos.
- **Testimonios con años de relación**: el dato "12 años de colaboración" es más potente que un simple testimonio anónimo.
- **Propuesta B2B diferenciada**: la sección de despachos tiene un discurso distinto al de particulares, lo que aumenta la relevancia percibida.

---

## 3. Aspectos a mejorar (existentes)

### Prioridad alta

| Problema | Impacto | Solución sugerida |
|----------|---------|-------------------|
| **El formulario no envía realmente** | Muy alto — leads perdidos | Conectar a Formspree, EmailJS, Netlify Forms o backend propio |
| **Email en hotmail.com** | Alto — daña percepción profesional | Migrar a `magdalena@escuderonocea.es` o similar |
| **Sin Google Maps / geolocalización** | Alto — clientes no saben llegar | Embeber mapa o al menos un enlace a Google Maps |
| **Sin etiqueta de teléfono "haz clic para llamar"** | Medio — en móvil el teléfono debería ser tap-to-call | El `href="tel:..."` ya está, verificar que ambos números lo usen |
| **Testimonios sin foto ni verificación** | Medio — podrían parecer inventados | Añadir fotos de perfil (con permiso) o logos de despachos |
| **SEO muy básico** | Medio | Ver sección 4 |

### Prioridad media

| Problema | Impacto | Solución sugerida |
|----------|---------|-------------------|
| Foto hero oculta en móvil (`display:none`) | Medio | Versión optimizada para móvil en lugar de ocultarla |
| Sin favicon | Bajo-medio | Generar favicon desde el logo |
| Sin `lang` en las páginas internas (no aplica aún) | Bajo | Tiene `lang="es"` en el html, correcto |
| Animaciones muy largas en carga (3+ segundos) | Medio | Reducir delays del hero, el usuario espera demasiado para ver contenido |
| Sin `aria-label` en la mayoría de elementos interactivos | Bajo-medio | Accesibilidad y SEO técnico |

---

## 4. Secciones / funcionalidades a añadir

### A. SEO y presencia digital

- **Open Graph / Twitter Cards**: metaetiquetas para que el link quede bien al compartirse en WhatsApp, LinkedIn, etc.
- **Schema.org (JSON-LD)**: marcar la página como `LegalService` con `@type: LegalService`, dirección, teléfono, áreas. Google puede mostrarlo en resultados enriquecidos.
- **Sitemap.xml y robots.txt**: necesarios si se quiere indexar correctamente.
- **Google Search Console + Analytics**: para medir tráfico y comportamiento.
- **Google My Business**: ficha de empresa en Google Maps — crítico para búsquedas locales "procurador Sevilla".

### B. Secciones nuevas de contenido

**Blog / Artículos jurídicos** *(captación orgánica)*
- Posts cortos explicando conceptos: "¿Qué es un monitorio?", "¿Qué pasa si no contesto una demanda?", "Cómo funciona la ejecución de sentencia"
- Atrae tráfico SEO de cola larga sin coste publicitario
- Posiciona a Magdalena como autoridad en el sector

**Zona de recursos descargables** *(lead magnet)*
- Guía PDF: "Qué es un procurador y por qué lo necesita"
- Checklist: "Documentos que necesita para presentar una demanda"
- A cambio del email → construcción de base de datos

**Mapa de juzgados / infografía** *(útil + SEO local)*
- Mapa visual de los juzgados de Sevilla con los que trabaja
- Refuerza la autoridad local y es contenido único

**Casos de éxito** (anónimos por confidencialidad)
- "Procedimiento de divorcio con custodia disputada — resultado favorable en 8 meses"
- Sin nombres, solo tipo de caso, jurisdicción, resultado y tiempo
- Mucho más concreto que los testimonios actuales

### C. Funcionalidades a añadir

**Reserva de primera consulta online**
- Calendly embebido o similar
- Permite al cliente elegir día/hora sin llamar
- Reduce fricción, especialmente para particulares que no quieren llamar en frío

**Chat en vivo o bot de pre-cualificación**
- Un chatbot simple (Tidio, Crisp) que recoja: nombre, tipo de asunto, urgencia
- Pre-cualifica el lead antes de que llegue a Magdalena
- Especialmente útil fuera de horario

**Área privada para despachos colaboradores** *(largo plazo)*
- Portal de seguimiento de expedientes
- Los despachos podrían ver el estado de sus asuntos sin tener que llamar
- Diferenciador enorme frente a la competencia

**Newsletter para letrados**
- Email mensual con novedades procesales relevantes (jurisprudencia, cambios de ley)
- Mantiene el contacto con despachos que no tienen un asunto activo en ese momento
- Plataforma: Mailchimp o Brevo (gratuitas hasta X suscriptores)

**WhatsApp Business con catálogo**
- Migrar el número a WhatsApp Business
- Configurar respuestas automáticas fuera de horario
- Catálogo de servicios visible desde el perfil

### D. Confianza y conversión

**Contador de casos / procedimientos** *(si hay datos)*
- "Más de 2.000 procedimientos gestionados" — cifra concreta impacta más que adjetivos

**Logos de despachos colaboradores**
- Con permiso, una franja de logos de despachos con los que trabaja
- Prueba social muy potente en el segmento B2B

**Sello de colegiación verificable**
- Enlace directo al registro oficial del Colegio de Procuradores de Sevilla con su ficha
- Transparencia radical que muy pocos hacen

**Garantía explícita**
- "Si no respondemos en 24 horas, llamamos nosotros" — compromiso concreto y memorable

---

## 5. Priorización recomendada

### Fase 1 — Inmediata (sin coste o coste mínimo)
1. Conectar el formulario a un servicio real (Formspree es gratis y lleva 15 minutos)
2. Crear ficha en Google My Business
3. Añadir Open Graph y Schema.org al HTML
4. Favicon
5. Migrar email a dominio profesional

### Fase 2 — Corto plazo (1–2 meses)
6. Embeber Google Maps en la sección de contacto
7. Añadir Calendly para reserva de consulta
8. Logos o avatares a los testimonios
9. 3–5 artículos de blog básicos (SEO local)

### Fase 3 — Medio plazo (3–6 meses)
10. Guía PDF descargable (lead magnet)
11. WhatsApp Business con auto-respuesta
12. Newsletter mensual para despachos
13. Casos de éxito anónimos

### Fase 4 — Largo plazo
14. Portal de seguimiento para despachos colaboradores
15. Blog consolidado con plan editorial
16. Campañas de Google Ads locales (Sevilla + keywords procesales)

---

*Documento generado el 24 de junio de 2026 a partir del análisis del archivo `index.html`.*
