# directorio-lenga

Sitio de **www.directoriolenga.cl**, el directorio web de Mapa Castro 2027 (Lenga Editorial y Turismo SpA, Chiloé).

Por ahora es un **demo en desarrollo**: una sola página estática que muestra las secciones previstas para el lanzamiento (directorio de avisadores con fichas Destacada/Estándar/Básica, sección del mapa impreso, info práctica, buses, eventos, blog y contacto). Los contenidos y fichas son referenciales.

## Estructura

```
index.html   página completa (HTML + CSS + JS, sin dependencias de build)
assets/      logos, favicon, fotos y textura del footer
```

## Uso

No requiere instalación: abre `index.html` en el navegador. Para publicar, se sube la carpeta tal cual a Netlify y se apunta el dominio desde NIC Chile.

El sitio lleva `noindex` mientras esté en desarrollo; quitarlo antes del lanzamiento.

## Analítica

La página integra Google Analytics 4 sin dependencias adicionales. Para activarlo:

1. Crea una propiedad GA4 y un flujo web para el dominio publicado.
2. Copia el ID de medición (`G-...`) en `GA_MEASUREMENT_ID`, al final de `index.html`, reemplazando `G-XXXXXXXXXX`.
3. Publica el sitio y comprueba en **Informes > Tiempo real** que aparezcan `page_view` y los eventos al navegar, recorrer secciones o usar los CTA y enlaces de contacto.
4. Para analizar los parámetros `section_id`, `location`, `method` y `category`, regístralos como dimensiones personalizadas en GA4.

El placeholder deja la analítica completamente inactiva: no carga el script de Google ni envía datos. GA4 registra automáticamente `page_view`; el sitio también envía `section_view`, `navigation_click`, `directory_category_select`, `directory_cta_click`, `lead_cta_click` y `generate_lead` (con método `email` o `whatsapp`). Antes de activarlo, publica el aviso de privacidad correspondiente y revisa los requisitos de consentimiento aplicables a tu audiencia.

Contacto: contacto@lengaeditorial.cl
