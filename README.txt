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
  la marca porque el sitio trata de un fabricante concreto): "Tu Kobold
  no funciona. ¿Merece la pena repararlo?" (7 palabras). Tamaño del H1
  aumentado: clamp(38-58px) → clamp(46-74px) en escritorio, 40px → 48px
  en móvil.

Variables SMTP en Vercel (ya configuradas, sin cambios):
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com
