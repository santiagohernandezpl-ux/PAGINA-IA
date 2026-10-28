# ☕ cafeYA

> Conectando los mejores granos de pequeños caficultores colombianos directamente con tu taza bajo estrictos estándares de comercio justo.

**cafeYA** es una plataforma web moderna e interactiva diseñada como una landing page de una sola página (*single-page application*). Su objetivo principal es visibilizar el trabajo de caficultores locales en Colombia, ofreciendo café de especialidad de alta trazabilidad y cortando intermediarios para asegurar una retribución justa a las familias productoras.

---

## 🚀 Características Principales

* **Navbar Fija y Responsive:** Barra de navegación superior con diseño adaptativo e incluye un menú hamburguesa interactivo controlado mediante JavaScript puro para dispositivos móviles.
* **Diseño Visual Atractivo (Hero Section):** Encabezado con imagen de fondo inmersiva de cafetales colombianos, capa translúcida para contraste óptimo y llamadas a la acción (*CTAs*) claras.
* **Catálogo de Cafés Campesinos:** Tarjetas de productos en rejilla adaptativa (*grid*) de 1 columna (móvil), 2 (tablet) y 3 (escritorio), que incluyen notas de cata, altitud, precios en pesos colombianos (COP) y efectos visuales al pasar el cursor (*hover*).
* **Manifiesto e Historia:** Sección informativa de doble columna que detalla el impacto social y económico del modelo de comercio directo.
* **Acordeón FAQ Interactivo:** Preguntas frecuentes desplegables controladas por JavaScript para resolver dudas sobre envíos, orígenes y frescura.
* **Formulario de Pedidos con Validación:** Formulario completo con validación en tiempo real para campos obligatorios, verificación de formato de correo electrónico, control de cantidades (1 a 10 unidades) y mensajes de error detallados.
* **Notificaciones Toast:** Alerta flotante verde de confirmación que aparece al enviar un pedido con éxito y desaparece automáticamente a los 4 segundos.
* **Modo Oscuro / Claro:** Botón dedicado para alternar instantáneamente entre temas utilizando las variantes nativas de Tailwind CSS.

---

## 🛠️ Tecnologías y Herramientas Utilizadas

* **HTML5:** Estructura semántica y accesible (cumplimiento con estándares WCAG).
* **Tailwind CSS 4:** Framework de estilos mediante el **Play CDN oficial** (`@tailwindcss/browser@4`) utilizando la directiva `@theme` para la paleta de colores personalizada.
* **JavaScript (Vanilla / Puro):** Lógica interactiva para el menú móvil, acordeón FAQ, validación de formularios y gestión de temas de color.
* **Google Fonts:** Tipografías tipográficas *Playfair Display* (para títulos elegantes) e *Inter* (para lectura general).
* **Unsplash:** Imágenes de ejemplo de alta calidad y temática cafetera.

---

## 🎨 Paleta de Colors Personalizada (`@theme`)

El proyecto está diseñado bajo una identidad visual cálida inspirada en la tierra y el grano de café:

* **Crema Claro (`#FAF8F5`):** Color dominante de fondo en modo claro (60%).
* **Café Tierra Profundo (`#2C1810`):** Color secundario para textos principales, navbar y footer (30%).
* **Ocre / Naranja Tostado (`#D97706`):** Color de acento para botones, insignias y llamadas a la acción (10%).
* **Verde Éxito (`#16A34A`):** Color semántico para toasts y confirmaciones.
* **Rojo Error (`#DC2626`):** Color semántico para alertas de validación en formularios.

---

## ⚙️ Cómo Ejecutar el Proyecto Localmente

No se requiere instalar Node.js, compiladores ni dependencias complejas ya que utiliza el CDN de Tailwind. Sigue estos sencillos pasos:

1. Clona este repositorio o descarga los archivos en tu ordenador.
2. Asegúrate de tener un archivo llamado `index.html` en el directorio raíz.
3. Haz doble clic sobre el archivo `index.html` o arrástralo y suéltalo dentro de cualquier navegador web moderno (**Google Chrome, Mozilla Firefox, Microsoft Edge o Safari**).
4. ¡Listo! La página web cargará instantáneamente con todas sus funcionalidades interactivas.

---

## 📂 Estructura del Código en el Archivo `index.html`

El proyecto se encuentra contenido en un único archivo modularizado y comentado en español de la siguiente manera:
1. `<head>` y Configuración del Tema `@theme` con Tailwind CSS 4.
2. **Navbar Fija** con enlace al menú móvil y botón de modo oscuro.
3. **Sección Hero** con imagen de fondo y botones de acción.
4. **Catálogo de Cafés** con tarjetas responsivas.
5. **Sección Nuestra Historia / Manifiesto**.
6. **Preguntas Frecuentes (FAQ)** con acordeón interactivo.
7. **Formulario de Pedidos** con validación y toast flotante de éxito.
8. **Pie de Página (Footer)** con enlaces, datos de contacto y redes sociales.
9. **Script de JavaScript** al cierre del `<body>` que controla la interactividad completa.

---

## 👤 Autor

Desarrollado con dedicación para enaltecer el trabajo del campo colombiano y la ingeniería de software accesible.

---

## 📄 Licencia

Este proyecto se distribuye bajo los términos de la licencia MIT. Siéntete libre de utilizarlo, modificarlo y adaptarlo para iniciativas de comercio justo.