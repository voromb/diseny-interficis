## 1. Introducción

Este proyecto corresponde a la asignatura **Diseño de Interfaces Web**. El objetivo ha sido construir una interfaz web sencilla, clara y responsive utilizando dos enfoques:

- Una versión con **HTML + CSS** en la carpeta `html-css/`.
- Una versión equivalente con **Tailwind CSS** en la carpeta `tailwind/`.

### Objetivos del proyecto

- Practicar la maquetación de una interfaz web.
- Aplicar diseño responsive para escritorio, tablet y móvil.
- Tener en cuenta principios básicos de accesibilidad (estructura semántica, contraste, textos alternativos).
- Mostrar el uso de un framework de utilidades (**Tailwind**) para reproducir el mismo diseño, utilizando únicamente la versión CDN para evitar instalar Node u otras herramientas.

### Alcance y limitaciones

- La web es **estática**: no hay base de datos ni servidor.
- No se implementan procesos reales de compra/venta ni dashboards.
- El foco está en el **diseño visual, la maquetación y la accesibilidad básica**, no en la lógica de negocio, que se desarrolla en las asignaturas de programación en servidor y en cliente.

### Metodología de trabajo

- **Análisis de usuarios**: se ha pensado en usuarios que consultan la web tanto desde escritorio como desde móvil, priorizando la claridad del contenido.
- **Capacidades visuales**: se han elegido colores con buen contraste, tamaños de fuente cómodos y estructura clara para facilitar la lectura, pensando en usuarios con posibles dificultades visuales.

---

## 2. Fundamentos del Diseño de Interfaces Web

### Interacción persona-ordenador (IPO)

La interfaz se ha diseñado para que la interacción entre la persona y la página sea sencilla:

- Estructura clara: cabecera, navegación, contenido principal y pie de página.
- Enlaces y botones con texto claro y acciones predecibles (“Ver más detalles”, “Enviar”).

### Principios de usabilidad aplicados

- **Facilidad**: navegación simple con tres páginas (Inicio, Sobre nosotros, Contacto).
- **Eficiencia**: el usuario encuentra rápidamente la información principal en la portada.
- **Satisfacción**: diseño limpio, colores coherentes y disposición ordenada de secciones.
- **Aprendizaje**: la estructura se repite en todas las páginas, lo que facilita recordar cómo moverse por la web.

### Psicología del usuario y experiencia de usuario (UX)

- Se ha priorizado una jerarquía visual clara (títulos, subtítulos, párrafos y tarjetas).
- Se muestra un resumen inicial en la portada, detalles en la página "Sobre nosotros" y un formulario sencillo en "Contacto".

> **Modo oscuro**: no se ha implementado modo oscuro; se ha optado por un modo claro con buen contraste.

---

## 3. Planificación del Proyecto

### Requerimientos funcionales

- Mostrar información del proyecto (quién lo realiza, objetivos y requisitos).
- Incluir una galería de imágenes y un vídeo demostrativo.
- Proporcionar un formulario de contacto accesible (aunque no envíe datos reales).
- Ofrecer dos implementaciones de la misma interfaz: HTML+CSS y Tailwind.

### Requerimientos no funcionales

- Diseño responsive (adaptación a escritorio, tablet y móvil).
- Accesibilidad básica (estructura semántica, `aria-labelledby`, `alt` en imágenes, mensaje alternativo en vídeo).
- Código legible y organizado en carpetas.

### Usuarios y escenarios de uso

- **Profesorado**: revisar el proyecto como ejercicio de segudno de DAW, comprobando diseño, maquetación y accesibilidad.
- **Alumnado/compañeros**: consultar el ejemplo de interfaz y la guía de estilos.

Flujo básico:

- Inicio → ver resumen, características, galería y vídeo.
- Sobre nosotros → leer explicación detallada y requisitos (RA1–RA6).
- Contacto → rellenar un formulario de ejemplo.

---

## 4. Componentes de la Interfaz Web

- **Elementos de identificación y branding**:
  - Título "Proyecto Web" en la cabecera de todas las páginas.

- **Elementos de navegación**:
  - Menú superior con enlaces a Inicio, Sobre nosotros y Contacto.
  - Página activa destacada con borde inferior azul.
  - En la versión HTML+CSS se incluye un menú hamburguesa para pantallas pequeñas.

- **Elementos de interacción**:
  - Botón principal "Ver más detalles" en la portada.
  - Formulario de contacto con campos de texto, email, select y textarea.
  - Botón "Enviar".

- **Contenidos principales y secundarios**:
  - Contenido principal: descripción del proyecto, características, requisitos y demo en vídeo.
  - Contenido secundario: pie de página con información resumida del proyecto.

- **Pie de página**:
  - Texto de resumen tipo "Proyecto de interfaz web · HTML y CSS" o "HTML y Tailwind" según versión.
  - Diseño consistente en todas las páginas.

---

## 5. Diseño Visual y Maquetación

### Principios aplicados

- **Proximidad y alineación (Gestalt)**: elementos relacionados se agrupan en secciones (tarjetas de características, lista de requisitos, galería, formulario).
- **Contraste**: texto oscuro sobre fondo claro en el contenido; texto claro sobre fondo oscuro en cabecera y pie.
- **Jerarquía visual**: uso de tamaños de fuente distintos para `h1`, `h2`, `h3` y párrafos.

### Guía de estilos (HTML+CSS y Tailwind)

**Tipografía y base**

- **Fuente base**: `system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`.
- **Tamaño base**: `16px`.
- **Interlineado**: `1.5`.
- **Color de texto principal**: `#111827`.
- **Color de fondo principal**: `#f9fafb`.

**Colores principales**

- **Fondo cabecera y pie**: `#111827`.
- **Texto cabecera y pie**: `#f9fafb`.
- **Degradado del hero**:
  - Azul oscuro: `#1d4ed8`.
  - Azul medio: `#3b82f6`.
- **Enlace activo en la navegación**: `#60a5fa` (borde inferior).
- **Texto secundario / descripciones**: tonos gris `#4b5563` / `#6b7280` (según componente).

En la versión Tailwind estos colores se aplican con clases utilitarias y valores hexadecimales (`bg-[#111827]`, `text-[#f9fafb]`, etc.).

**Layout general**

- **Ancho máximo del contenido**: aprox. `960px`, centrado horizontalmente.
- **Espaciado lateral**: padding horizontal alrededor de `1.5rem`–`1.75rem`.
- **Secciones**:
  - Separadas entre sí con margen inferior (~`2rem`).
  - Títulos (`h1`, `h2`) con margen inferior (`1rem`).

**Cabecera y navegación**

- Cabecera en la parte superior de cada página:
  - Fondo oscuro (`#111827`).
  - Título de proyecto a la izquierda.
  - Menú de navegación a la derecha.
- Navegación:
  - Versión HTML+CSS: lista `<ul>` horizontal con `display: flex` y `gap` entre elementos.
  - Versión Tailwind: `flex` + `gap` en el `<ul>`.
  - Página activa marcada con **borde inferior azul** (`border-bottom` / `border-[#60a5fa]`).

En la versión HTML+CSS hay un menú hamburguesa responsive controlado con un `<input type="checkbox">` y media queries.

**Hero (portada)**

- Bloque principal destacado en la portada (`index`):
  - Fondo con **degradado azul diagonal**.
  - Texto en color claro (`#f9fafb`).
  - Esquinas redondeadas (~`1rem`).
- Contenido:
  - Título principal (`h1`) con tamaño fluido (`clamp` en CSS / tamaño equivalente en Tailwind).
  - Párrafo descriptivo del proyecto.
  - Botón de acción "Ver más detalles".

**Botón principal**

- Versión HTML+CSS (`.boton-primario`):
  - Fondo claro `#f9fafb`.
  - Texto azul `#1d4ed8`.
  - Borde muy redondeado (pastilla).
  - Hover: fondo `#e5e7eb`.
- Versión Tailwind: mismas ideas con clases (`bg-[#f9fafb]`, `text-[#1d4ed8]`, `rounded-full`, `hover:bg-[#e5e7eb]`).

### Wireframes y prototipado

No se han incluido wireframes ni prototipos interactivos en el repositorio. El diseño se ha trabajado directamente en HTML+CSS y luego trasladado a Tailwind.

---

## 6. Accesibilidad Web

- Se han tenido en cuenta las siguientes ideas de accesibilidad (inspiradas en WCAG):
  - Uso de etiquetas semánticas (`header`, `main`, `section`, `footer`).
  - Uso de `aria-labelledby` para vincular secciones con sus títulos.
  - Textos `alt` descriptivos en las imágenes.
  - Mensaje alternativo dentro de las etiquetas `<video>`.
  - Colores con suficiente contraste entre texto y fondo.

No se realiza una auditoría completa de WCAG ni se implementa toda la normativa (LSSI, etc.), pero sí se aplican buenas prácticas básicas.

---

## 7. Diseño Responsive y Adaptativo

- **Principios de responsive design**:
  - Uso de `flex`, `grid` y `media queries` (en CSS) y utilidades responsive (en Tailwind) para adaptar el contenido.
  - La galería y las tarjetas pasan de varias columnas a una sola en pantallas pequeñas.

- **Mobile-first y progressive enhancement**:
  - El diseño se ha probado en diferentes anchos de pantalla.
  - Se prioriza que el contenido sea legible en móviles y se enriquece en pantallas más grandes.

---

## 8. Framework para layouts adaptativos: Tailwind

- En la carpeta `tailwind/` se replica la misma interfaz utilizando **Tailwind CSS** cargado por CDN.
- Se han ajustado las clases de Tailwind para que el resultado visual sea muy similar a la versión HTML+CSS.
- Se reutiliza la misma paleta de colores y la misma estructura de contenido.

---

## 9. Arquitectura de la Información y Navegación

- **Mapa de navegación sencillo**:
  - `index.html` → portada con hero, características, galería e introducción al vídeo.
  - `sobre.html` → detalles del proyecto y requisitos (RA1–RA6).
  - `contacto.html` → formulario de contacto de ejemplo.

- **Organización de contenidos**:
  - De lo más general (portada) a lo más detallado (sobre el proyecto y requisitos).
  - Acceso directo al formulario desde el menú superior.

- **Jerarquía visual**:
  - Títulos grandes para secciones principales.
  - Tarjetas y listas para agrupar información relacionada.

---

## 10. Demo final (sin base de datos ni servidor)

Este proyecto no implementa procesos reales de compra/venta ni dashboards como en una aplicación tipo Vinted. En su lugar, se muestra una **demo estática** que podría ser la base de una interfaz más compleja:

- Presentación de la interfaz en diferentes tamaños de pantalla mediante imágenes y un vídeo.
- Ejemplo de formulario de contacto accesible.

No hay perfil de usuario, histórico de compras/ventas ni paneles con gráficas.

---

## 11. Anexos

### Glosario de términos (breve)

- **Responsive design**: diseño que se adapta automáticamente al tamaño de la pantalla.
- **Accesibilidad web**: conjunto de técnicas para que la web sea usable por el mayor número de personas posible.
- **Tailwind CSS**: framework de utilidades CSS que permite maquetar usando clases en el HTML.

### Bibliografía y recursos utilizados

- Documentación oficial de MDN Web Docs (HTML y CSS).
- Documentación oficial de Tailwind CSS.
- Apuntes de la asignatura de Diseño de Interfaces Web.

### Documentación técnica complementaria

- Estructura de carpetas:
  - `html-css/`: versión HTML+CSS del sitio.
  - `tailwind/`: versión equivalente con Tailwind.
  - `assets/img/`: imágenes usadas en la galería.
  - `assets/media/`: vídeo de demostración.

Esta documentación, junto con el código, completa la entrega del proyecto.
