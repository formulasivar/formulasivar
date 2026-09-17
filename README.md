# Formula Sivar — Comunidad de Fórmula 1 en El Salvador

Sitio web oficial de **Formula Sivar**, la comunidad de Fórmula 1 y Motor Sport en El Salvador. Landing page estática con información de la comunidad, calendario de eventos, cobertura de Grandes Premios, podcast, radio y accesos a redes sociales.

**Sitio en producción:** https://formulasivar.com

## Contenido del sitio

- **Inicio (`index.html`):** presentación de la comunidad, accesos a redes sociales, próximos eventos y calendario de la temporada.
- **Calendario 2026 (`temp-2026.html`):** calendario interactivo de carreras y actividades.
- **Grandes Premios (`gp-brasil.html`, etc.):** páginas de cobertura por evento con diseño dedicado.
- **Podcast (`podcast.html`):** episodios y enlaces de escucha.
- **Radio (`radio.html`):** reproductor y banners destacados en el home.
- **Landyard (`landyard.html`):** página de producto con secciones alternadas.

Redes integradas: Instagram, Telegram, WhatsApp (canal), TikTok, YouTube, Amazon Shop, Google Calendar y podcast propio.

## Características técnicas

- **Sitio 100 % estático:** HTML, CSS y JavaScript vanilla, sin frameworks ni dependencias de build. Carga rápida y hosting gratuito.
- **Responsive:** layout bento en desktop (2 columnas) y apilado en móvil, con banners dedicados (`banner_desktop.webp` / `banner_Web.webp`).
- **Estilos:** efecto glassmorphism, CSS modular por página (`global.css`, `home.css`, `calendar-2026.css`, `podcast.css`, `radio.css`, `landyard.css`).
- **Interactividad:** contador de eventos, slider de calendario y reproductor de radio en JS vanilla (`app.js`, `calendar-interaction.js`, `radio.js`).
- **SEO:** meta tags, Open Graph / Twitter Cards, `robots.txt`, `sitemap.xml` e H1 semántico.
- **Analítica:** Umami (`cloud.umami.is`) para medición de visitas sin cookies invasivas.
- **Assets optimizados:** imágenes WebP, iconografía propia y caché de navegador vía `.htaccess` (aplica solo en hostings Apache; sin efecto en GitHub Pages).

## Estructura del proyecto

```text
├── index.html          # Home
├── temp-2026.html      # Calendario temporada
├── gp-brasil.html      # Cobertura por GP (plantilla por evento)
├── podcast.html        # Podcast
├── radio.html          # Radio
├── landyard.html       # Página de producto
├── css/                # Estilos modulares
├── js/                 # Lógica vanilla
├── assets/             # icons, images, videos, Escuderias, radio_audio, animations
├── CNAME               # Dominio personalizado (formulasivar.com)
├── robots.txt
├── sitemap.xml
```

## Desarrollo local

No requiere instalación. Clona y sirve la carpeta con cualquier servidor estático:

```bash
git clone git@github.com:formulasivar/formulasivar.git
cd formulasivar
python3 -m http.server 8000
# Abrir http://localhost:8000
```

## Despliegue

- **Hosting:** GitHub Pages, repositorio `formulasivar/formulasivar`, rama `main`, fuente `Deploy from branch` (`/(root)`).
- **Dominio:** `formulasivar.com` configurado vía archivo `CNAME` + registros DNS (4x `A @` de GitHub Pages y `CNAME www` a `formulasivar.github.io`), con `Enforce HTTPS` activo.
- **Flujo de publicación:** cada `push` a `main` redespliega automáticamente. No hay CI adicional.

## Contribución

1. Crea una rama desde `main` para tu cambio.
2. Previsualiza en local antes de subir.
3. Abre un Pull Request describiendo el cambio y las páginas afectadas.
4. Mantén imágenes en WebP y actualiza `sitemap.xml` (`lastmod`) si agregas páginas públicas.

## Licencia y contacto

Código del sitio con todos los derechos reservados para la comunidad Formula Sivar, salvo indicación contraria. Para eventos, alianzas o prensa, contactar por los canales oficiales enlazados en https://formulasivar.com.

