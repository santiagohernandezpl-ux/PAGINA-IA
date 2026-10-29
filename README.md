# ☕ cafeYA — Landing Page

Landing page de **cafeYA**, una plataforma web para descubrir, conocer la historia y pedir cafés 100% campesinos directamente de productores locales de Colombia. Está pensada para amantes del café, consumidores conscientes y turistas que valoran el comercio justo.

---

## 📋 Contenido

- [Características](#-características)
- [Tecnologías](#-tecnologías)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Cómo ejecutarlo](#-cómo-ejecutarlo)
- [Secciones de la página](#-secciones-de-la-página)
- [Paleta de colores y tipografía](#-paleta-de-colores-y-tipografía)
- [Accesibilidad](#-accesibilidad)
- [Personalización](#-personalización)
- [Limitaciones conocidas](#-limitaciones-conocidas)
- [Créditos](#-créditos)

---

## ✨ Características

- Diseño **mobile-first** y totalmente responsive.
- **Modo claro / oscuro** con la variante `dark:` de Tailwind. La preferencia se guarda en el navegador y, la primera vez, respeta la configuración del sistema.
- **Menú hamburguesa** interactivo en móviles (se cierra con la tecla `Escape`).
- **Catálogo** en rejilla de 1 / 2 / 3 columnas con efectos *hover*.
- **Acordeón FAQ** controlado con JavaScript (un panel abierto a la vez).
- **Formulario de pedidos** con validación en JavaScript, mensajes de error en rojo y un **toast verde** que desaparece a los 4 segundos.
- Contador de carrito con anuncios para lectores de pantalla.
- Un único archivo, **sin dependencias de terceros** ni proceso de compilación.

## 🛠 Tecnologías

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura semántica |
| [Tailwind CSS 4](https://tailwindcss.com/) (Play CDN) | Estilos y tema personalizado con `@theme` |
| JavaScript puro (Vanilla JS) | Interactividad y validación |
| [Google Fonts](https://fonts.google.com/) | *Playfair Display* (títulos) e *Inter* (texto) |
| [Unsplash](https://unsplash.com/) | Imágenes de ejemplo |

## 📁 Estructura del proyecto

```
cafeya/
├── index.html   # Página completa: HTML, tema de Tailwind y JavaScript
└── README.md    # Este archivo
```

## 🚀 Cómo ejecutarlo

> Necesitas conexión a internet: Tailwind, las fuentes y las imágenes se cargan desde CDN.

**Opción 1 — Directo en el navegador**
1. Descarga o clona el proyecto.
2. Haz doble clic en `index.html` (o arrástralo a Chrome, Firefox o Edge).

**Opción 2 — Con servidor local (recomendado para desarrollo)**
- **VS Code:** instala la extensión *Live Server*, clic derecho en `index.html` → *Open with Live Server*.
- **Python:**
  ```bash
  python -m http.server 8000
  ```
  Luego abre `http://localhost:8000`.
- **Node.js:**
  ```bash
  npx serve .
  ```

## 🧩 Secciones de la página

1. **Navbar fija:** logo en texto, enlaces a cada sección, contador de carrito, botón de tema y botón "Pedir Café".
2. **Hero:** título, subtítulo, imagen de cafetal con capa oscura y botones "Ver Catálogo" y "Conocer la Historia".
3. **Nuestros Cafés Campesinos:** 6 tarjetas con imagen, finca o vereda, notas de cata, precio en COP y botón "Añadir al carrito".
4. **Nuestra Historia / Manifiesto:** texto e imagen en dos columnas (una en móvil) sobre el comercio directo.
5. **Preguntas Frecuentes:** acordeón de 4 preguntas.
6. **Formulario de pedido:** nombre, correo, dirección, variedad y cantidad (1 a 10).
7. **Footer:** enlaces rápidos, contacto, redes sociales y derechos reservados.

## 🎨 Paleta de colores y tipografía

Definida con `@theme` dentro de `<style type="text/tailwindcss">` siguiendo la regla 60-30-10:

| Rol | Token | Color |
|---|---|---|
| Dominante (60%) | `crema` | `#FAF8F5` |
| Secundario (30%) | `tierra` | `#2C1810` |
| Acento (10%) | `ocre` | `#D97706` |
| Éxito | `exito` | `#16A34A` |
| Error | `error` | `#DC2626` |

**Tonos auxiliares para cumplir el contraste 4.5:1:**

| Token | Color | Por qué |
|---|---|---|
| `ocre-oscuro` | `#B45309` | El ocre base sobre crema da ~3:1; este tono se usa para textos de acento. |
| `ocre-claro` | `#F59E0B` | Texto de acento sobre fondos oscuros. |
| `error-texto` | `#B91C1C` | Mensajes de error legibles sobre blanco. |
| `exito-oscuro` | `#15803D` | Fondo del toast con texto blanco. |

**Tipografía:** `font-display` → Playfair Display · `font-sans` → Inter.

## ♿ Accesibilidad

- Textos alternativos (`alt`) en todas las imágenes; iconos decorativos con `aria-hidden`.
- Cada campo del formulario tiene su `<label>`; los errores se asocian con `aria-describedby` y `aria-invalid`.
- Enfoque visible (`:focus-visible`) en todos los elementos interactivos.
- Enlace "Saltar al contenido principal" para usuarios de teclado.
- Menú y acordeón con `aria-expanded` y `aria-controls`.
- Toast y carrito anunciados mediante regiones `aria-live`.
- Respeta `prefers-reduced-motion`.

## 🔧 Personalización

| Qué cambiar | Dónde |
|---|---|
| Colores y fuentes | Bloque `@theme` en el `<head>` |
| Imágenes | Atributos `src` (y `alt`) y el `style` del Hero |
| Productos | Duplicar un `<li>` en la sección `#cafes` y añadir la `<option>` en el formulario |
| Preguntas FAQ | Copiar un bloque y actualizar `id`, `aria-controls` y `aria-labelledby` |
| Reglas y mensajes de validación | Objeto `reglas` en el `<script>` |
| Duración del toast | `setTimeout(..., 4000)` en `mostrarToast()` |
| Datos de contacto y redes | Sección `<footer>` (los enlaces `href="#"` son de ejemplo) |

## ⚠️ Limitaciones conocidas

- **El envío del formulario es simulado.** Para recibir pedidos reales, reemplaza el bloque "Envío exitoso" del script por un `fetch()` hacia tu backend o un servicio de formularios.
- El carrito solo cuenta productos; no guarda los artículos ni calcula el total.
- El **Play CDN de Tailwind** está pensado para prototipos. Para producción, se recomienda instalar Tailwind con su CLI o Vite y generar un CSS optimizado.
- Las imágenes de Unsplash son de ejemplo; reemplázalas por fotos propias de los productores.

## 🙌 Créditos

- Imágenes: [Unsplash](https://unsplash.com/) (licencia gratuita).
- Fuentes: [Google Fonts](https://fonts.google.com/).
- Estilos: [Tailwind CSS](https://tailwindcss.com/).

---

© 2026 cafeYA. Todos los derechos reservados.
