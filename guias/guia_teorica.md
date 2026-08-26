# Guía Teórica: Fundamentos de HTML, CSS y Estructura de Proyectos

¡Hola! Para construir sitios web exitosos, es indispensable comprender las bases teóricas y la lógica detrás del código. En esta guía aprenderás qué es HTML y CSS, cómo se conectan entre sí, y cuáles son las etiquetas y propiedades más utilizadas en el desarrollo web.

---

## 🏛️ 1. ¿Qué es HTML y CSS?

Para entender el desarrollo frontend, imagina que estás construyendo una casa:

> [!NOTE]
> ### 🧱 HTML (HyperText Markup Language)
> **Es el esqueleto o la estructura de la casa.** 
> Define dónde van las vigas, las paredes, las puertas y las ventanas. HTML no se encarga de la estética, sino de ordenar y jerarquizar los elementos de la página (textos, imágenes, enlaces, menús, etc.).

> [!TIP]
> ### 🎨 CSS (Cascading Style Sheets)
> **Es la decoración, pintura y terminaciones de la casa.** 
> Define los colores de las paredes, los materiales de los pisos, la tipografía de los letreros y la distribución espacial de los muebles. Con CSS controlamos la presentación visual y la adaptabilidad a diferentes pantallas (responsive design).

---

## 📁 2. Estructura y Conexión de Carpetas (Rutas Relativas)

Para que el navegador muestre tu web correctamente, debe leer los archivos en su respectivo orden. Los proyectos web deben organizarse en carpetas y conectarse mediante **rutas relativas**.

### 💻 Ejemplo de Estructura de Carpetas:
```text
mi-sitio-web/
│
├── index.html          👈 Archivo HTML en la raíz del proyecto
│
├── css/
│   └── style.css       👈 Archivo de estilos dentro de la carpeta "css"
│
└── img/
    └── avatar.jpg      👈 Foto de perfil dentro de la carpeta "img"
```

### 🔗 ¿Cómo se conectan en el código HTML?
Dado que tu archivo `index.html` está en la raíz, debe "entrar" a las subcarpetas para encontrar los recursos:

1.  **Conectar la Hoja de Estilos (CSS):** Dentro de la etiqueta `<head>` de tu HTML:
    ```html
    <link rel="stylesheet" href="css/style.css">
    ```
2.  **Mostrar una Imagen:** Dentro del `<body>` de tu HTML:
    ```html
    <img src="img/avatar.jpg" alt="Foto de perfil de Carolina">
    ```

---

## ⚙️ 3. Estructura del Código

HTML y CSS tienen reglas de escritura específicas que debes seguir para evitar errores:

### A. Anatomía de una Etiqueta HTML
La mayoría de las etiquetas HTML tienen apertura, contenido y cierre. También pueden incluir **atributos** que configuran su comportamiento:

```text
  Etiqueta de                      Etiqueta de
   Apertura          Contenido       Cierre
  ┌────────┐       ┌───────────┐    ┌─────────┐
   <p class="bio">  Hola, mundo.     </p>
   └─┬──┘ └───┬──┘
     │        └─ Valor del Atributo (en comillas)
     └─ Nombre del Atributo (class, href, src, etc.)
```

### B. Anatomía de una Regla CSS
En CSS seleccionamos un elemento de HTML (por su etiqueta, clase o ID) y le aplicamos estilos abriendo llaves `{}`:

```text
 Selector           Propiedad          Valor
┌────────┐         ┌─────────┐      ┌─────────┐
  .card      {     background-color: #ffffff;      }
                   └────────────────────────┘
                       Declaración (Termina en ;)
```

---

## 🎨 4. ¿Cómo funcionan los colores en CSS y HTML?

En CSS podemos definir colores para textos (`color`), fondos (`background-color`), bordes (`border-color`), sombras, etc. Existen diferentes métodos para declarar los colores según tus necesidades y la transparencia que quieras darles:

### A. Nombres de Colores (Named Colors)
Son nombres predefinidos en inglés por el navegador. Son muy fáciles de usar, pero bastante limitados (existen 140 nombres).
*   **Ejemplos:** `color: red;`, `background-color: blue;`, `color: transparent;`

### B. Sistema Hexadecimal (HEX)
Es el formato más utilizado en la web. Utiliza códigos de base 16 (números del `0` al `9` y letras de la `A` a la `F`) precedidos por un `#`.
*   **Estructura:** `#RRGGBB` (donde `RR` es Red/Rojo, `GG` es Green/Verde y `BB` es Blue/Azul). Cada par va desde `00` (sin color) hasta `FF` (máxima intensidad).
*   **Con Transparencia (Alpha):** Se añade un cuarto par opcional al final `#RRGGBBAA`.
*   **Ejemplos:**
    *   `#ffffff` (Blanco)
    *   `#000000` (Negro)
    *   `#4a3aff` (Azul eléctrico)
    *   `#4a3aff80` (Azul eléctrico con **50% de opacidad**)

### C. Sistema RGB y RGBA
Mezcla intensidades de Rojo (Red), Verde (Green) y Azul (Blue) usando números del `0` al `255`.
*   **Estructura:** `rgb(R, G, B)` o `rgba(R, G, B, A)` para añadir el canal **Alpha** (transparencia) con valores decimales entre `0.0` (totalmente transparente) y `1.0` (totalmente opaco).
*   **Ejemplos:**
    *   `rgb(255, 255, 255)` (Blanco)
    *   `rgb(0, 0, 0)` (Negro)
    *   `rgba(74, 58, 255, 0.5)` (Azul eléctrico con **50% de opacidad**)

### D. Sistema HSL y HSLA
Es el sistema más cómodo y visual. Divide el color en Tono (Hue), Saturación (Saturation) y Luminosidad (Lightness).
*   **Estructura:** `hsl(Tono, Saturación%, Luminosidad%)`
    *   **Tono:** Grados en el círculo cromático (`0` a `360`). `0` es rojo, `120` es verde y `240` es azul.
    *   **Saturación:** `%` de intensidad del color (`0%` escala de grises, `100%` color saturado).
    *   **Luminosidad:** `%` de brillo/luz (`0%` negro absoluto, `100%` blanco absoluto).
    *   **Alpha:** Se añade el canal transparente: `hsla(T, S%, L%, A)`.
*   **Ejemplos:**
    *   `hsl(245, 100%, 61%)` (Azul eléctrico)
    *   `hsla(245, 100%, 61%, 0.3)` (Azul eléctrico con **30% de opacidad**)

---

## 🏷️ 5. Diccionario de Etiquetas HTML más Frecuentes

Para organizar tu información de forma clara, aquí tienes una tabla con las etiquetas estructuradas que más utilizarás:

### 🏠 Estructura General y Semántica
| Etiqueta | 📝 Propósito Semántico | 💡 Ejemplo de Uso |
| :--- | :--- | :--- |
| `<!DOCTYPE html>` | Declara al navegador que el archivo es un documento HTML5. | Colocado en la primera línea del archivo. |
| `<html>` | Nodo raíz que envuelve todo el contenido del sitio web. | `<html lang="es"> ... </html>` |
| `<head>` | Contiene metadatos invisibles para el usuario (links CSS, título de pestaña). | `<head> <title>Mi web</title> </head>` |
| `<body>` | Contenedor de todo el contenido visible en la página web. | `<body> <h1>Hola</h1> </body>` |
| `<main>` | Define la sección con el contenido principal y exclusivo de la página. | `<main> <article>...</article> </main>` |
| `<header>` | Cabecera del sitio o de una sección (ej. menú o banner superior). | `<header> <nav>...</nav> </header>` |
| `<nav>` | Define bloques de navegación del sitio (menús de enlaces). | `<nav> <a href="#">Inicio</a> </nav>` |
| `<footer>` | Pie de página (créditos, copyright, enlaces de pie). | `<footer> © 2026 Carolina Torres </footer>` |
| `<section>` | Agrupa contenido relacionado de manera temática o lógica. | `<section> <h2>Sobre mí</h2> </section>` |

### ✍️ Contenido y Texto
| Etiqueta | 📝 Propósito Semántico | 💡 Ejemplo de Uso |
| :--- | :--- | :--- |
| `<h1>` a `<h6>` | Encabezados de títulos. `<h1>` es el más importante; `<h6>` el menor. | `<h1>Carolina Torres</h1>` |
| `<p>` | Define un párrafo de texto normal. | `<p>Me apasiona el diseño digital...</p>` |
| `<ul>` | Lista desordenada (se muestra con puntos o viñetas por defecto). | `<ul> <li>Elemento</li> </ul>` |
| `<li>` | Define cada uno de los elementos de una lista (`<ul>` o `<ol>`). | `<li>Instagram</li>` |
| `<a>` | Enlace o hipervínculo. Requiere `href` para indicar la URL. | `<a href="https://linkedin.com">LinkedIn</a>` |
| `<img>` | Inserta una imagen. Requiere `src` (ruta) y `alt` (texto alternativo). | `<img src="img/avatar.jpg" alt="Foto">` |
| `<div>` | Contenedor genérico en bloque. Agrupa elementos para dar estilos. | `<div class="avatar-container">...</div>` |
| `<hr>` | Crea una línea horizontal que separa temáticamente el contenido. | `<hr class="separator">` |

---

## 🎨 6. Diccionario de Propiedades CSS más Frecuentes

Controla los espacios, colores y el diseño de tus elementos con estas propiedades clave:

### 📦 Caja y Espaciado (Modelo de Caja)
| Propiedad | 🎨 Descripción | 💡 Ejemplo de Uso |
| :--- | :--- | :--- |
| `width` | Define el ancho de un elemento (en `px`, `%`, `vw`, etc.). | `width: 350px;` |
| `max-width` | Establece el ancho máximo (evita desbordamientos en pantallas pequeñas). | `max-width: 600px;` |
| `height` | Define el alto de un elemento (en `px`, `%`, `vh`, etc.). | `height: 150px;` |
| `padding` | Espacio **interno** entre el borde de la caja y su contenido. | `padding: 20px;` |
| `margin` | Espacio **externo** entre esta caja y sus elementos vecinos. | `margin: 0 auto;` (Centra bloques) |
| `border` | Aplica un borde alrededor de la caja. Define grosor, estilo y color. | `border: 2px solid #4a3aff;` |
| `box-sizing` | Modifica el cálculo del tamaño de la caja para incluir bordes y paddings. | `box-sizing: border-box;` (¡Obligatorio!) |

### 🧩 Layout y Alineación (Flexbox)
| Propiedad | 🎨 Descripción | 💡 Ejemplo de Uso |
| :--- | :--- | :--- |
| `display` | Define el tipo de comportamiento de caja del elemento. | `display: flex;` (Activa Flexbox) |
| `justify-content` | Alinea los elementos a lo largo del **eje principal** (horizontal). | `justify-content: center;` |
| `align-items` | Alinea los elementos a lo largo del **eje secundario** (vertical). | `align-items: center;` |
| `flex-direction` | Define la orientación de los elementos hijos (en fila o columna). | `flex-direction: column;` |
| `gap` | Espaciado directo entre los elementos hijos de un contenedor Flex. | `gap: 15px;` |

### 🔤 Texto y Tipografía
| Propiedad | 🎨 Descripción | 💡 Ejemplo de Uso |
| :--- | :--- | :--- |
| `color` | Define el color del texto. | `color: #475569;` |
| `font-family` | Aplica la familia tipográfica (fuente) al texto. | `font-family: 'Outfit', sans-serif;` |
| `font-size` | Cambia el tamaño de la letra. | `font-size: 16px;` |
| `font-weight` | Controla el grosor de las letras (grosor de 100 a 900). | `font-weight: 700;` (Negrita) |
| `text-align` | Modifica la alineación horizontal del texto. | `text-align: center;` |
| `text-decoration` | Agrega o quita decoraciones de texto (como el subrayado). | `text-decoration: none;` (Quita subrayados) |

### ✨ Decoración y Efectos Visuales
| Propiedad | 🎨 Descripción | 💡 Ejemplo de Uso |
| :--- | :--- | :--- |
| `background-color`| Modifica el color de fondo de un elemento. | `background-color: #ffffff;` |
| `border-radius` | Redondea las esquinas de los bordes (usa `50%` para círculos). | `border-radius: 12px;` |
| `box-shadow` | Crea una sombra alrededor de la caja para dar efecto de relieve. | `box-shadow: 0 4px 20px rgba(0,0,0,0.05);`|
| `transition` | Define una animación de transición para suavizar cambios de estado. | `transition: all 0.3s ease;` |
