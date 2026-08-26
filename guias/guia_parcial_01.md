# Guía de Aprendizaje: Entrega Parcial 01 — Portafolio Web Final

¡Felicidades! Has llegado a la fase final de construcción de tu primer sitio web personal. El propósito de esta entrega parcial es **consolidar y perfeccionar tu proyecto**, experimentando activamente con **efectos especiales de animación**, **responsividad completa** y la estructuración de **código semántico**.

Esta entrega representa el **40% de la nota final** (40 puntos en total).

---

## 🎯 Objetivos de la Entrega
1. **HTML Semántico:** Reemplazar el uso genérico de `<div>` por etiquetas con significado estructural (`header`, `nav`, `main`, `section`, `article`, `footer`).
2. **Responsive Design (Adaptabilidad):** Asegurar que tu sitio se vea impecable en computadores de escritorio y celulares, adaptando el contenedor central sin generar scroll horizontal ni textos desbordados.
3. **Efectos de Animación (AOS):** Integrar la librería **Animate On Scroll (AOS)** en al menos 3 elementos para dar dinamismo al portafolio.
4. **Interactividad CSS:** Agregar estados visuales (`:hover` y transiciones) en todos los enlaces, botones y menús.
5. **Aplicación de Feedback:** Resolver y corregir todos los errores detectados por la profesora en las formativas anteriores.

---

## 🏗️ 1. Estructura y Código Semántico HTML5
En esta etapa final es obligatorio que tu código describa la **estructura y significado** de tu contenido. 

### 💡 Ejemplo de Maquetación Semántica:
*   **Antes (Solo `<div>`):**
    ```html
    <div class="header"> <!-- No aporta significado -->
        <div class="menu">...</div>
    </div>
    ```
*   **Ahora (Semántica HTML5 - Correcto):**
    ```html
    <header class="main-header">
        <nav class="nav-menu">
            <a href="index.html">Inicio</a>
            <a href="proyectos.html">Proyectos</a>
            <a href="contacto.html">Contacto</a>
        </nav>
    </header>
    ```

Asegúrate de aplicar:
*   `<main>` para el contenedor o card central.
*   `<section>` para separar grandes bloques de contenido (como la biografía o el listado de proyectos).
*   `<article>` para cada tarjeta de proyecto individual.
*   `<footer>` para el pie de página y créditos.

---

## 📱 2. Responsive Design (Adaptación a Celulares)
Tu sitio debe ser **mobile-first** o adaptarse fluidamente en dispositivos pequeños sin provocar scroll horizontal.

### 📝 Lista de control para Responsive:
*   **Contenedor Central:** En desktop mantendrá un ancho elegante (ej: `max-width: 800px;` o `max-width: 1000px;`), pero en celulares debe ajustarse usando porcentajes (`width: 90%` o `width: 95%`) y tener márgenes laterales adecuados.
*   **Proyectos:** En pantallas de escritorio pueden organizarse en columnas (2 o 3 columnas), pero en celulares deben pasar a **una sola columna** (apilados verticalmente).
*   **Imágenes:** Deben escalar de forma fluida (usando `max-width: 100%; height: auto;`) para que no se deformen ni salgan de sus cajas.
*   **Formulario:** Los campos de texto del formulario de contacto deben ocupar el 100% del ancho del contenedor en dispositivos móviles.

### 💡 Código CSS responsivo de referencia:
```css
/* Media query para pantallas de celular (ancho máximo de 768px) */
@media (max-width: 768px) {
    /* La cuadrícula de proyectos pasa a una columna */
    .projects-grid {
        grid-template-columns: 1fr;
    }
    
    /* El contenedor central adapta sus márgenes */
    main.card {
        width: 95%;
        margin: 20px auto;
        padding: 15px;
    }
}
```

---

## ⚡ 3. Animaciones con AOS (Animate On Scroll)
Para darle un look moderno y premium a tu portafolio, utilizaremos **AOS**, una librería ligera que activa animaciones a medida que el usuario hace scroll en la página.

### 🔌 Paso 1: Vincula AOS mediante CDN
Agrega estas líneas en el archivo HTML de cada una de tus páginas:

1.  **En el `<head>` (Estilos CSS de AOS):**
    ```html
    <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />
    ```
2.  **Antes de cerrar la etiqueta `</body>` (Código JavaScript de AOS):**
    ```html
    <script src="https://unpkg.com/aos@next/dist/aos.js"></script>
    <script>
        AOS.init({
            duration: 800, /* Duración de la animación en milisegundos */
            once: true /* La animación ocurre solo una vez al hacer scroll */
        });
    </script>
    ```

### 🏷️ Paso 2: Aplica los atributos de animación
Añade el atributo `data-aos` a los elementos HTML que desees animar (mínimo 3 en todo el sitio). Ejemplos:
```html
<article class="project-card" data-aos="fade-up">
    <!-- Contenido del proyecto -->
</article>

<div class="contact-form" data-aos="zoom-in">
    <!-- Formulario -->
</div>
```

---

## ✨ 4. Interactividad CSS (:hover y Transiciones)
Los elementos interactivos deben reaccionar suavemente a la acción del cursor del usuario:

```css
/* Estilo base para el botón de enviar */
.btn-submit {
    background-color: #001F3F; /* Tu color secundario/primario */
    color: #F6F7ED;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease, transform 0.2s ease; /* Transición suave */
}

/* Estado hover (cuando el mouse pasa sobre el botón) */
.btn-submit:hover {
    background-color: #DBE64C; /* Tu color de acento brillante */
    color: #001F3F;
    transform: translateY(-2px); /* Pequeño salto visual */
}
```

---

## 🛠️ Rúbrica de Evaluación (40 Puntos)

| Criterio | Logro completo | Logro parcial | Logro insuficiente | Máx |
| :--- | :--- | :--- | :--- | :---: |
| **Estructura HTML** | HTML5 semántico (`header`, `nav`, `main`, `footer`) y bien organizado. | Errores de semántica o estructuración. | Errores semánticos graves o ausencia de etiquetas HTML5. | **6 pts** |
| **CSS y presentación** | Diseño coherente, personalizado, pulido y limpio. | Inconsistencias visuales menores o estilos descuidados. | CSS incompleto o mal estructurado. | **4 pts** |
| **Funcionamiento** | Enlaces funcionales, imágenes con `alt` y formulario validado. | Errores menores en rutas o carga de assets. | Errores graves de navegación o enlaces rotos. | **5 pts** |
| **Responsive** | Se adapta a móviles y escritorios sin scroll horizontal ni textos cortados. | Problemas menores de adaptación en resoluciones específicas. | No adaptado / se rompe en vistas móviles. | **5 pts** |
| **Librería AOS** | Integración y personalización autónoma de AOS en al menos 3 elementos. | Implementación con errores menores de sincronización o sobrecargada. | AOS no implementado o no funciona. | **4 pts** |
| **Mejoras aplicadas** | Implementa mejoras según feedback previo y las sugerencias de las guías de estudio. | Pocas mejoras o correcciones aplicadas. | Ignora el feedback anterior y las guías. | **4 pts** |
| **Git y proceso** | Mínimo 3 nuevos commits descriptivos (mínimo 9 en todo el proceso). | Commits escasos o mensajes genéricos. | Sin historial estructurado de avance en Git. | **3 pts** |
| **Publicación final** | Publicación final impecable en GitHub Pages. | Errores menores de carga remota de recursos. | Inaccesible en línea. | **3 pts** |
| **Autoaprendizaje y Documentación** | Documenta formalmente en el README o bitácora cómo investigó y resolvió de forma autónoma los desafíos de diseño responsivo o librerías externas. | Documenta superficialmente sus hallazgos y fuentes. | No evidencia aprendizaje autónomo ni documenta su proceso. | **6 pts** |

---

## 📋 Checklist antes de entregar:
- [ ] ¿El menú de navegación conecta perfectamente las 3 páginas de ida y vuelta?
- [ ] ¿El sitio funciona y se lee bien en celulares (sin desbordes ni scroll horizontal)?
- [ ] ¿El contenedor central disminuye proporcionalmente su ancho en mobile?
- [ ] ¿Reemplazaste los divs genéricos por etiquetas semánticas (`header`, `main`, `footer`, etc.)?
- [ ] ¿Las imágenes tienen atributo `alt` y cargan correctamente en internet?
- [ ] ¿Los botones y enlaces tienen efectos hover interactivos con transiciones CSS?
- [ ] ¿Vinculaste la librería AOS (CSS en `<head>` y JS en la parte inferior del `<body>`)?
- [ ] ¿La animación AOS está funcionando correctamente en al menos 3 elementos?
- [ ] ¿El repositorio de GitHub está ordenado con carpetas `/css` y `/img`?
- [ ] ¿Agregaste la sección de "Desafíos y Autoaprendizaje" en tu README o bitácora para explicar qué aprendiste e investigaste solo?
- [ ] ¿Tienes al menos 9 commits en total (mínimo 3 nuevos en esta entrega)?
- [ ] ¿Verificaste el enlace final de tu GitHub Pages en tu celular o simulador del navegador?

---

## 🛠️ Herramientas recomendadas para probar responsividad
Para verificar que tu sitio web sea realmente responsivo y se adapte de forma correcta a múltiples dispositivos sin desbordarse:
1. **[Responsively App](https://responsively.app/):** Una aplicación de escritorio excelente e indispensable para desarrolladores web. Te permite ver tu sitio web reflejado en múltiples pantallas de diferentes tamaños de celulares y tablets al mismo tiempo. ¡Cualquier interacción o scroll se replica simultáneamente en todas las pantallas!
2. **Responsive Viewer (Extensión de Chrome):** Si prefieres no instalar una aplicación separada, puedes buscar e instalar la extensión de Chrome llamada **Responsive Viewer**. Funciona directamente dentro del navegador y te permite visualizar múltiples pantallas responsive de forma paralela en una sola pestaña.
