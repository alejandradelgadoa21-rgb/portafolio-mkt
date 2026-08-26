# Guía Teórica: Fundamentos de HTML, CSS y Estructura de Proyectos

¡Hola! Para construir sitios web exitosos, es indispensable comprender las bases teóricas y la lógica detrás del código. En esta guía aprenderás qué es HTML y CSS, cómo se conectan entre sí, y cuáles son las etiquetas y propiedades más utilizadas en el desarrollo web.

---

## 🏛️ 1. ¿Qué es HTML y CSS?

Para entender el desarrollo frontend, imagina que estás construyendo una casa:

*   **HTML (HyperText Markup Language - Lenguaje de Marcado de Hipertexto):** Es la **estructura o esqueleto** de la casa. Define dónde van las paredes, las puertas, las ventanas y las habitaciones. HTML no se encarga del aspecto visual, sino de organizar y jerarquizar el contenido (textos, imágenes, menús, etc.).
*   **CSS (Cascading Style Sheets - Hojas de Estilo en Cascada):** Es la **decoración y pintura** de la casa. Define de qué color se pintan las paredes, qué tipo de piso se coloca, el tamaño de las ventanas y la distribución de los muebles. Con CSS le damos estilo, colores, tipografía, espacios y adaptabilidad (responsive design) a la estructura HTML.

---

## 📁 2. Estructura y Conexión de Carpetas (Rutas Relativas)

Para que el navegador pueda mostrar tu sitio web, necesita leer los archivos HTML, CSS y las imágenes. Para ello, los archivos deben estar organizados en carpetas y conectados correctamente mediante **rutas relativas**.

### Ejemplo de Estructura de un Proyecto:
```text
mi-sitio-web/
│
├── index.html          <-- Está en la raíz del proyecto
│
├── css/
│   └── style.css       <-- Adentro de la carpeta "css"
│
└── img/
    └── avatar.jpg      <-- Adentro de la carpeta "img"
```

### 🔗 ¿Cómo se conectan en el código?
Dado que `index.html` está en la raíz, debe "entrar" a las subcarpetas para encontrar los otros archivos:

1.  **Vincular el CSS:** En tu `index.html` (dentro de la etiqueta `<head>`), le indicas al navegador que busque la carpeta `css` y luego el archivo `style.css`:
    ```html
    <link rel="stylesheet" href="css/style.css">
    ```
2.  **Mostrar una Imagen:** En tu `index.html` (dentro de `<body>`), indicas que busque en la carpeta `img` y luego el archivo `avatar.jpg`:
    ```html
    <img src="img/avatar.jpg" alt="Foto de perfil">
    ```

---

## ⚙️ 3. Estructura del Código

Tanto HTML como CSS tienen su propia sintaxis o forma de escribirse:

### A. Anatomía de una Etiqueta HTML
Una etiqueta HTML suele estar compuesta por una etiqueta de apertura, contenido, y una etiqueta de cierre. Además, puede contener atributos (como `class` o `href`):

```text
  Etiqueta de                      Etiqueta de
   Apertura          Contenido       Cierre
  ┌────────┐       ┌───────────┐    ┌─────────┐
   <p class="bio">  Hola, mundo.     </p>
   └─┬──┘ └───┬──┘
     │        └─ Valor del Atributo
     └─ Nombre del Atributo
```

### B. Anatomía de una Regla CSS
En CSS seleccionamos un elemento de HTML (usando su etiqueta o clase) y le aplicamos estilos abriendo y cerrando llaves `{}`:

```text
 Selector           Propiedad          Valor
┌────────┐         ┌─────────┐      ┌─────────┐
  .card      {     background-color: #ffffff;      }
                   └────────────────────────┘
                       Declaración (Termina en ;)
```

---

## 🏷️ 4. Diccionario de Etiquetas HTML más Frecuentes

Aquí tienes las etiquetas esenciales que utilizarás para estructurar tus páginas:

### Estructura General y Semántica
*   `<!DOCTYPE html>`: Le indica al navegador que el documento es un archivo HTML5.
*   `<html>`: Contenedor principal de todo el documento.
*   `<head>`: Contiene información invisible para el usuario, pero clave para el navegador (título de la pestaña, enlaces a hojas de estilo, tipografías).
*   `<body>`: Contiene todo lo que el usuario ve en pantalla (textos, imágenes, botones).
*   `<main>`: Define el contenido principal y único de la página.
*   `<header>`: Cabecera o encabezado de la página o de una sección.
*   `<nav>`: Contenedor para los enlaces de navegación (menús).
*   `<footer>`: Pie de página (créditos, copyright, enlaces secundarios).
*   `<section>`: Agrupa temáticas o secciones lógicas dentro de la página.

### Contenido y Texto
*   `<h1>` a `<h6>`: Encabezados o títulos. El `<h1>` es el más importante (título principal) y `<h6>` el de menor jerarquía.
*   `<p>`: Define un párrafo de texto.
*   `<ul>`: Crea una lista desordenada (con viñetas).
*   `<li>`: Define un elemento dentro de una lista (`<ul>` o `<ol>`).
*   `<a>`: Enlace o hipervínculo. Requiere el atributo `href` para indicar el destino (ej. `<a href="https://google.com">Google</a>`). Usa el atributo `target="_blank"` para abrirlo en una pestaña nueva.
*   `<img>`: Inserta una imagen. Es una etiqueta auto-conclusiva (no tiene cierre `</img>`). Requiere el atributo `src` (ruta del archivo) y `alt` (texto descriptivo para accesibilidad).
*   `<div>`: Un contenedor genérico en bloque. Se usa para agrupar elementos y aplicarles estilos o layouts con CSS.
*   `<hr>`: Crea una línea horizontal divisoria.

---

## 🎨 5. Diccionario de Propiedades CSS más Frecuentes

Estas son las propiedades básicas que emplearás para dar estilo y estructurar tus componentes:

### Caja y Espaciado (Modelo de Caja)
*   `width`: Ancho de un elemento (puede expresarse en píxeles `px` o en porcentajes `%`).
*   `max-width`: Establece el ancho máximo que puede alcanzar un elemento (clave para responsive design).
*   `height`: Alto de un elemento.
*   `padding`: Espacio interno de un elemento (la distancia entre el contenido y su borde).
*   `margin`: Espacio externo de un elemento (la distancia entre el elemento y otros elementos vecinos).
*   `border`: Define el borde de un elemento. Se compone de grosor, estilo y color (ej. `border: 1px solid #000000;`).
*   `box-sizing: border-box;`: Propiedad fundamental que asegura que el `padding` y el `border` se incluyan dentro del tamaño total (`width`) del elemento, evitando que este se agrande innecesariamente.

### Diseño y Flexbox (Distribución)
*   `display`: Controla el comportamiento de visualización de un elemento.
    *   `display: block;`: El elemento ocupa todo el ancho de la línea.
    *   `display: inline;`: El elemento solo ocupa el espacio de su contenido.
    *   `display: flex;`: Activa Flexbox para organizar de manera flexible los elementos hijos.
*   `justify-content`: En Flexbox, alinea los elementos hijos a lo largo del **eje principal** (horizontal por defecto). Valores comunes: `center`, `flex-start`, `flex-end`, `space-between`.
*   `align-items`: En Flexbox, alinea los elementos hijos a lo largo del **eje secundario** (vertical por defecto). Valores comunes: `center`, `stretch`, `flex-start`.
*   `flex-direction`: Define la dirección en la que se colocan los elementos hijos dentro de un contenedor Flexbox (ej. `row` para filas, `column` para columnas).
*   `gap`: Define la separación o espacio entre los elementos hijos de un contenedor Flexbox o Grid.

### Texto y Tipografía
*   `color`: Modifica el color del texto.
*   `font-family`: Define la fuente o tipografía del texto.
*   `font-size`: Define el tamaño de la letra (ej. `16px`, `1.2rem`).
*   `font-weight`: Establece el grosor de la letra (ej. `300` para delgada, `400` para regular, `700` para negrita).
*   `text-align`: Alinea el texto de manera horizontal (`left`, `center`, `right`, `justify`).
*   `text-decoration`: Permite añadir o quitar decoraciones al texto (muy usada como `text-decoration: none;` para quitar el subrayado automático a los enlaces).

### Decoración y Estética
*   `background-color`: Define el color de fondo de un elemento.
*   `border-radius`: Redondea las esquinas de un elemento (usa `50%` para convertir cajas perfectamente cuadradas en círculos).
*   `box-shadow`: Añade sombras alrededor de un elemento para darle profundidad visual.
*   `transition`: Permite suavizar los cambios de propiedades (por ejemplo, hacer que el cambio de color al pasar el mouse sobre un botón tarde `0.3s` en vez de ser instantáneo).
