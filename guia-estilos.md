# Guía de estilos del proyecto

Este documento resume de forma sencilla los estilos utilizados en el proyecto, tanto en la versión **HTML + CSS** (`html-css/`) como en la versión **Tailwind** (`tailwind/`).

## 1. Tipografía y base

- **Fuente base**: `system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`.
- **Tamaño base**: `16px`.
- **Interlineado**: `1.5`.
- **Color de texto principal**: `#111827`.
- **Color de fondo principal**: `#f9fafb`.

## 2. Colores principales

- **Fondo cabecera y pie**: `#111827`.
- **Texto cabecera y pie**: `#f9fafb`.
- **Degradado del hero**:
  - Azul oscuro: `#1d4ed8`.
  - Azul medio: `#3b82f6`.
- **Enlace activo en la navegación**: `#60a5fa` (borde inferior).
- **Texto secundario / descripciones**: tonos gris `#4b5563` / `#6b7280` (según componente).

En la versión Tailwind estos colores se aplican con clases utilitarias y valores hexadecimales (`bg-[#111827]`, `text-[#f9fafb]`, etc.).

## 3. Layout general

- **Ancho máximo del contenido**: aprox. `960px`, centrado horizontalmente.
- **Espaciado lateral**: padding horizontal alrededor de `1.5rem`–`1.75rem`.
- **Secciones**:
  - Separadas entre sí con margen inferior (~`2rem`).
  - Títulos (`h1`, `h2`) con margen inferior (`1rem`).

## 4. Cabecera y navegación

- Cabecera fija en la parte superior de cada página:
  - Fondo oscuro (`#111827`).
  - Título de proyecto a la izquierda.
  - Menú de navegación a la derecha.
- Navegación:
  - Versión HTML+CSS: lista `<ul>` horizontal con `display: flex` y `gap` entre elementos.
  - Versión Tailwind: `flex` + `gap` en el `<ul>`.
  - Página activa marcada con **borde inferior azul** (`border-bottom` / `border-[#60a5fa]`).

En la versión HTML+CSS hay un menú hamburguesa responsive controlado con un `<input type="checkbox">` y media queries.

## 5. Hero (portada)

- Bloque principal destacado en la portada (`index`):
  - Fondo con **degradado azul diagonal**.
  - Texto en color claro (`#f9fafb`).
  - Esquinas redondeadas (~`1rem`).
- Contenido:
  - Título principal (`h1`) con tamaño fluido (`clamp` en CSS / tamaño equivalente en Tailwind).
  - Párrafo descriptivo del proyecto.
  - Botón de acción "Ver más detalles".

### Botón principal

- Versión HTML+CSS (`.boton-primario`):
  - Fondo claro `#f9fafb`.
  - Texto azul `#1d4ed8`.
  - Borde muy redondeado (pastilla).
  - Hover: fondo `#e5e7eb`.
- Versión Tailwind: mismas ideas con clases (`bg-[#f9fafb]`, `text-[#1d4ed8]`, `rounded-full`, `hover:bg-[#e5e7eb]`).

## 6. Tarjetas de características

- Sección "Características principales":
  - Grid de **tres columnas en escritorio**, una columna en pantallas pequeñas.
  - Cada tarjeta:
    - Fondo blanco.
    - Esquinas redondeadas.
    - Sombra suave.
    - Título (`h3`) y párrafo descriptivo.

## 7. Galería de imágenes y vídeo

- Sección "Galería del diseño":
  - **Dos columnas** (escritorio), una columna en móvil.
  - Cada `figure` incluye:
    - Imagen (`img`) a ancho completo, con esquinas redondeadas.
    - `figcaption` con texto explicativo en tamaño más pequeño.
- Presentación en vídeo:
  - Vídeo a ancho completo máximo ~640px.
  - Recuadro con título, vídeo y descripción.
  - En HTML+CSS se usa `.video-proyecto`; en Tailwind se usa `w-full` + `rounded` para el vídeo.

## 8. Listas y texto en "Sobre nosotros"

- Sección descriptiva del proyecto con dos párrafos.
- Sección "Requisitos" con lista de resultados de aprendizaje (RA1–RA6):
  - Lista con viñetas (`disc`).
  - Espaciado vertical pequeño entre elementos.

## 9. Formulario de contacto

- Estructura común en ambas versiones:
  - Campos: Nombre, Correo electrónico, Motivo de contacto (select), Mensaje (textarea).
  - Botón "Enviar".
- Estilos de campos:
  - Bordes redondeados.
  - Borde gris claro.
  - Estado de foco con resaltado (borde/outline azul).
- Botón de envío:
  - Versión HTML+CSS: reutiliza el estilo de `.boton-primario`.
  - Versión Tailwind: botón azul con hover más oscuro y anillo de foco.

## 10. Multimedia

- Imágenes:
  - `assets/img/maqueta-escritorio.png`
  - `assets/img/maqueta-movil.png`
- Vídeo:
  - `assets/media/presentacion-proyecto.mp4`
- En ambos casos se cuida:
  - `alt` descriptivo en las imágenes.
  - Mensaje alternativo dentro de `<video>` para navegadores que no soporten vídeo HTML5.

---

