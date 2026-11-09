# Portafolio — Anthony Murillo Zapata

Sitio de portafolio bilingüe (ES/EN) construido a partir del CV y de la imagen de referencia
(`D:\Ejemplo base.webp`): fondo verde/negro, tarjetas redondeadas, marco claro, tipografía
geométrica y composición en dos columnas que se apila en móvil.

## Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | **El sitio completo**: HTML + CSS + JavaScript en un solo archivo. |
| `foto.jpeg` | Tu foto (se usa en el hero). |
| `cv.html` | Plantilla del CV en formato imprimible A4 (por si quieres regenerar el PDF). |
| `Anthony-Murillo-Zapata-CV.pdf` | CV de una página que descarga el botón "Descargar CV". |
| `fake CV.docx` | CV original que me diste (se conserva como referencia). |

## Cómo verlo

Doble clic en `index.html`. No necesita servidor ni instalar nada.

Para publicarlo: sube la carpeta a GitHub Pages, Netlify o Vercel (es estático).

## Qué incluye

- **Mobile first / responsive**: probado a 390, 768, 1024, 1360 y 1440 px sin scroll horizontal.
- **Bilingüe ES/EN** con selector en la navbar; recuerda el idioma en `localStorage` y detecta
  el idioma del navegador la primera vez.
- **Menú móvil** accesible (se abre/cierra, `aria-expanded`, cierra con Escape).
- Hero con foto, estadísticas, CTAs, redes y estado "disponible para prácticas".
- Sobre mí, servicios, experiencia, formación, referencias y formulario de contacto.
- Portafolio con filtros (Todos / Aeroespacial / Automoción / Operaciones) y botón "Ver más".
- Animaciones suaves (respeta `prefers-reduced-motion`).
- Formulario sin backend: valida y abre el cliente de correo (`mailto:`).

## Lo que debes personalizar

1. **Email**: busca `anthony@example.com` en `index.html` (aparece 3 veces) y pon el tuyo.
2. **LinkedIn**: busca `https://www.linkedin.com/` y `linkedin.com/in/anthony`.
3. **Foto**: reemplaza `foto.jpeg` por otra con el mismo nombre (idealmente vertical).
   El recorte se controla en `.hero__photo img` (`object-position` y `transform: scale()`).
4. **Empresa del CV**: el texto original usaba `NAME Commercials`; cámbialo por el nombre real
   en `DATA.exp` (inglés y español).
5. **Proyectos**: los 8 proyectos son ejemplos con miniaturas SVG hechas a mano. Para usar
   capturas reales, cambia el bloque `<div class="thumb">…</div>` por
   `<img src="assets/proyecto.jpg" alt="…">` y ajusta el CSS.
6. **CV PDF**: edita `cv.html` y vuelve a generar el PDF (o simplemente reemplaza
   `Anthony-Murillo-Zapata-CV.pdf` por tu CV definitivo).
7. **Referencias**: los nombres son genéricos ("Encargada de tienda", "Jefe de taller");
   pon nombres reales cuando los tengas.

## Dónde están los textos

Todo el contenido bilingüe está en el `<script>` al final de `index.html`:

- `I18N.en` / `I18N.es` → textos de interfaz y secciones.
- `DATA.services` → tarjetas de servicios.
- `DATA.work` → proyectos del portafolio.
- `DATA.exp` / `DATA.edu` → experiencia y formación.
- `DATA.refs` → referencias.
- `DATA.chips` → etiquetas del "Sobre mí".

Cada elemento visible tiene un `data-i18n="clave"`; si añades una clave nueva, agrégala en
ambos idiomas.

## Paleta y tipografías

- Fondo `#040605`, panel `#070908`, tarjetas `#121614`.
- Verdes `#02251a` → `#12a468`, acento menta `#7cf0b8`.
- Títulos: **Plus Jakarta Sans**; texto: **Inter** (Google Fonts con fallback del sistema).

## Nota

Las miniaturas del portafolio y el CV en PDF se generaron para este proyecto; no son capturas
de trabajos reales. Sustitúyelas por tus propios proyectos cuando los tengas.
