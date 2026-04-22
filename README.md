# GERENCIA.COM — Rediseño del sitio web

Rediseño completo, moderno y minimalista del sitio **gerenciasac.com**. Paleta y logo originales; copy e imágenes conservados; enfoque en conversión (CTAs claros, WhatsApp siempre disponible, formularios con destino directo al correo corporativo).

## Stack

- **100% estático**: HTML, CSS y JavaScript puros. Sin build step.
- **Tipografía**: Inter (Google Fonts).
- **Formularios**: [FormSubmit](https://formsubmit.co/) — envía directamente a `trade@gerenciasac.com`. Sin backend propio.
- **Compatibilidad**: todos los navegadores modernos; diseño responsive (mobile-first).

## Estructura

```
.
├── index.html                 # Homepage
├── gear.html                  # GEAR — Quiénes somos
├── servicios.html             # 9 servicios + giros de negocio
├── brochure.html              # Brochure corporativo
├── postula.html               # Postula Aquí (Trabaja con nosotros)
├── contacto.html              # Contáctanos (formulario + mapa)
├── gracias.html               # Página de agradecimiento post-formulario
├── 404.html                   # Página de error
├── blog/
│   ├── index.html             # Listado de artículos
│   ├── igv-hoteles-restaurantes-2026.html
│   ├── descanso-medico-depresion-ansiedad.html
│   └── descansos-medicos-subsidios-empleadores.html
└── assets/
    ├── css/styles.css         # Estilos
    ├── js/main.js             # JS (menú móvil, contadores, reveal on scroll, año dinámico)
    └── img/                   # Logo, fotos, íconos de servicios e industrias
```

## Activación de FormSubmit (paso único)

Los formularios apuntan a `https://formsubmit.co/trade@gerenciasac.com`. La primera vez que **alguien envíe** el formulario, FormSubmit enviará un **correo de confirmación** a `trade@gerenciasac.com` con un botón *“Activate FormSubmit”*. Haz clic una sola vez y a partir de ese momento todos los envíos llegarán directamente a la bandeja de entrada.

Pasos recomendados tras el despliegue:
1. Publicar el sitio (GitHub Pages, Netlify, Vercel, hosting tradicional — cualquiera sirve).
2. Abrir la página de **Contáctanos** y enviar un mensaje de prueba desde cualquier navegador.
3. Abrir `trade@gerenciasac.com`, revisar el correo de FormSubmit y pulsar **Activate FormSubmit**.
4. A partir de aquí, cualquier mensaje desde `/contacto.html` o postulación desde `/postula.html` se entregará al correo.

> Si prefieres anti-spam con CAPTCHA, cambia en los formularios:
> `<input type="hidden" name="_captcha" value="false" />` → `value="true"`.

## URL de redirección tras envío (`_next`)

Hoy los formularios redirigen a `https://gerenciasac.com/gracias.html`. Si el sitio vive en otro dominio temporalmente, edita ese valor en:
- `contacto.html` (línea del `<input name="_next">`)
- `postula.html` (línea del `<input name="_next">`)

## Redes sociales

Links ya conectados en nav, footer y barra superior:
- Facebook: `https://www.facebook.com/gerencia.com.pe`
- Instagram: `https://www.instagram.com/gerencia.com.pe/`
- LinkedIn: `https://www.linkedin.com/company/gerenciacom/`
- WhatsApp: `https://wa.me/51965353315`

## Contacto

- Tel: `044 – 612019`
- WhatsApp: `+51 965 353 315`
- Correo: `trade@gerenciasac.com`
- Oficina: Av. Teodoro Valcárcel 777, Urb. Primavera, Trujillo – Perú.

## Despliegue

### GitHub Pages (gratis)
1. En el repo, Settings → Pages → Source: `Deploy from a branch` → `main` → `/ (root)`.
2. Esperar 1–2 min. URL disponible en `https://zalocncn.github.io/gerencia/`.

### Netlify / Vercel (gratis con dominio personalizado)
1. Arrastrar la carpeta al dashboard o conectar el repo de GitHub.
2. No requiere build (proyecto estático).
3. Conectar el dominio `gerenciasac.com` en el panel.

### Hosting tradicional (cPanel, FTP)
Subir el contenido tal cual al directorio raíz (`public_html/`).

## Paleta y tipografía

- Azul marca: `#0033FF` (del logo)
- Azul oscuro: `#041A4D`
- WhatsApp: `#25D366`
- Tipografía: **Inter** 400/500/600/700/800.

## Licencia / atribuciones

- Imágenes y copy: propiedad de Gerencia SAC (GERENCIA.COM).
- Íconos inline SVG: creados ad-hoc para este sitio, libres de usar.
- Fuentes: Inter — licencia OFL.
