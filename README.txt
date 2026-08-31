KOBOLDTECH — SERVICIO TÉCNICO ASPIRADORES Y ROBOTS KOBOLD (MADRID)

Diagnóstico: 20 € + IVA
Teléfono: +34 914 46 85 03
El correo de soporte no aparece visible; solo se usa en backend.

Dominio:
https://koboldtech.com.es/
(revisado contra el resto de dominios de la familia en esta sesión;
no hay colisión)

HISTORIAL: el repositorio era multipágina (14 páginas /modelos/ para
gamas VR, VK, VT y EB, más varias páginas /servicios/) y se convirtió a
one-page; esas páginas fueron eliminadas en commits anteriores. Como
ya no existen en el sitemap actual, se ha añadido middleware.mjs para
redirigir (301) cualquier URL antigua a la home, evitando 404 en
enlaces indexados o backlinks antiguos. Excluye /api/* y cualquier
ruta con extensión de archivo. Se añadió "@vercel/functions": "^2.0.3"
a package.json como dependencia de esta función.

REVISIÓN (fixes aplicados):
- Schema.org: no existía. Añadido LocalBusiness JSON-LD (nombre, url,
  teléfono, dirección, areaServed, sameAs con Google Maps y YouTube).
- Sección SEO en la home: no existía. Añadida sección "Guía" (id="guia",
  enlazada en el menú) con contenido propio sobre gamas VR/VK/VT/EB,
  el coste del diagnóstico (20 € + IVA) y el proceso de recogida.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar /
  Política de privacidad → https://kelatos.com/privacy-policy/), con
  diseño apilado a ancho completo en móvil.
- Google Analytics: no existía. Añadido G-KRBGY9NQPG.
- Botón del chat: añadido border:1px solid #fff!important al selector
  del chat-window-toggle (regla CSS estándar de la familia).
- Botón de teléfono del menú (.navcall): el texto largo ("Atención
  Telefónica 24 horas 365 días") deformaba la píldora al envolverse en
  dos líneas. Acortado a solo el número (+34 914 46 85 03) y añadido
  white-space:nowrap como salvaguarda.
- H1 de portada reescrito, corto y directo (estilo Isra Bravo, incluye
  la marca porque el sitio trata de un fabricante concreto). Tamaño
  del H1 aumentado: clamp(38-58px) → clamp(46-74px) en escritorio,
  40px → 48px en móvil. Iterado en varios commits posteriores
  (afirmativo, sin interrogación, sin condicionales, sin "Descubre")
  hasta el texto final actual: "Tu Kobold no funciona. Aquí lo
  diagnosticamos y lo reparamos."

REVISIÓN ADICIONAL (esta pasada):
- Faltaban las etiquetas og:title/og:description/og:url/og:type y el
  meta robots (no existía ninguna). Añadidas.
- Actualizado el texto del H1 en este README, que documentaba una
  versión anterior y ya superada.
- Verificado: schema.org, sección SEO, banner de cookies, borde del
  chat, package.json y middleware ya estaban correctos; no se ha
  tocado nada más.

Variables SMTP en Vercel (ya configuradas, sin cambios):
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la plantilla "no funciona" usada en varios repos.
  Reescrito con síntoma específico: "Tu Kobold no aspira o se para
  solo. Lo diagnosticamos." (10 palabras).
- BUG REAL — quitada la etiqueta rotada del hero (.hero-pill,
  "Robots aspiradores · Aspiradores Kobold") que sobresalía y se
  solapaba con la caja de información en anchos de tablet, mismo
  patrón detectado hoy en AcerTech y otros repos (aquí con nombre de
  clase distinto: .hero-pill en vez de .hero-chip/.hero-tag).
- BUG REAL — dos textos decorativos gigantes sin reducción de tamaño
  en móvil/tablet: ".problems::after" ("KOBOLD", 180px) y
  ".care-art::before" ("LIMPIEZA", 88px). Añadida reducción en tablet
  (100px/56px) y móvil (60px/40px).
- BUG REAL — el formulario no tenía ninguna casilla de consentimiento
  de política de privacidad. Añadida, con enlace a
  https://kelatos.com/privacy-policy/ en azul y subrayado.
- Añadida franja de aviso de servicio técnico independiente debajo
  del menú (no existía).
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Botón "Atención Telefónica..." sin icono, a diferencia del de
  WhatsApp. Añadido (verificado con cuidado el cierre de </a>).
- Verificado: schema.org ya usaba correctamente el único teléfono que
  tiene este repo; formulario correctamente conectado a
  /api/contacto.
