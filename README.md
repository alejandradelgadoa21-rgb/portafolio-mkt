# Mi sitio web personal
## Evaluación de la unidad — HTML + CSS + GitHub

**Proyecto incremental · 100 puntos**

---

# ¿Qué vamos a construir?

Un sitio web personal compuesto por **3 páginas**:

- **Inicio:** presentación personal y redes.
- **Proyectos:** 3 proyectos destacados.
- **Contacto:** formulario de contacto.

Las tres vistas deben conservar como elemento principal un **contenedor o cuadrado central** que organiza el contenido del sitio.

El proyecto será construido utilizando:

- HTML
- CSS
- Librería de animaciones **AOS (Animate On Scroll)**
- Git
- GitHub
- GitHub Pages

> No utilizaremos frameworks de maquetación. El objetivo es comprender cómo construir un sitio desde cero con HTML y CSS, incorporando al final una librería externa sencilla de animaciones.

---

# El proyecto crece con cada entrega

No realizaremos tres proyectos diferentes.

Trabajaremos sobre **el mismo sitio durante toda la unidad**.

### Formativa 01 — 30 pts
Construir la página de inicio.
*Entrega: miércoles 2 de septiembre a las 23:00 hrs.*

### Formativa 02 — 30 pts
Completar el flujo del sitio.
*Entrega: miércoles 9 de septiembre a las 23:00 hrs.*

### Parcial — 40 pts
Agregar la librería de animaciones AOS, corregir las entregas anteriores y publicar la versión final.
*Entrega: 15 o 16 de septiembre hasta las 23:00 hrs.*

**Total: 100 puntos**

---

# Requisitos generales

En **cada entrega**:

- El proyecto debe estar almacenado en GitHub.
- El sitio debe estar publicado mediante GitHub Pages.
- Deben existir **mínimo 3 commits nuevos por entrega**.
- Los commits deben representar avances reales del trabajo.
- Los enlaces y rutas solicitadas deben funcionar.
- HTML y CSS deben estar correctamente vinculados.

Al finalizar el proyecto existirán, como mínimo, **9 commits** asociados a las tres entregas.

---

# Formativa 01
## Mi primera página — 30 puntos
**Fecha de entrega: miércoles 2 de septiembre a las 23:00 hrs.**

### Objetivo

Construir `index.html` y transformar una estructura HTML básica en una página personal.

La página debe contener una **card o contenedor principal ubicado al centro de la página**.

Este contenedor central será parte de la identidad estructural del proyecto y deberá mantenerse durante las siguientes entregas.

---

# Formativa 01
## ¿Qué debe contener?

### Presentación personal

- Fotografía, avatar o imagen.
- Nombre.
- Breve descripción personal/profesional.
- Área, intereses o especialidad.
- Mínimo 2 enlaces o redes sociales.

### Estructura

- HTML5.
- Archivo CSS externo.
- Card o contenedor principal centrado.
- Colores, tipografía y espacios personalizados.
- Enlaces funcionando.

Los **colores y tipografías son de libre elección**. Cada estudiante puede definir su propia propuesta visual.

---

# Formativa 01
## ¿Qué vamos a evaluar?

| Criterio | Puntaje |
|---|---:|
| Estructura HTML | 8 pts |
| Card de presentación | 8 pts |
| CSS y presentación visual | 6 pts |
| Git y GitHub — mínimo 3 commits | 5 pts |
| Publicación en GitHub Pages | 3 pts |
| **Total** | **30 pts** |

---

# Formativa 02
## Mi sitio personal — 30 puntos
**Fecha de entrega: miércoles 9 de septiembre a las 23:00 hrs.**

### Objetivo

Transformar nuestra página inicial en un **sitio web navegable**.

Ahora tendremos:

`index.html`

`proyectos.html`

`contacto.html`

Las tres páginas deben estar conectadas mediante una navegación común.

---

# Formativa 02
## Página de proyectos

La página debe presentar **3 proyectos destacados**.

Cada proyecto debe contener:

- Nombre.
- Breve descripción.
- Imagen.
- Enlace cuando corresponda.

Los proyectos deben estar organizados visualmente utilizando HTML y CSS.

---

# Formativa 02
## Página de contacto

Crear un formulario utilizando HTML.

Debe incluir como mínimo:

- Nombre.
- Correo electrónico.
- Mensaje.
- Botón enviar.

Los campos deben utilizar:

- `label`
- `input`
- `textarea`
- tipos de input apropiados
- `required` cuando corresponda

> El formulario no necesita enviar información realmente.

---

# Formativa 02
## Navegación

Todas las páginas deben permitir navegar entre:

**Inicio → Proyectos → Contacto**

Y también regresar a las páginas anteriores.

Además:

- No deben existir enlaces internos rotos.
- El CSS debe estar correctamente vinculado.
- Las imágenes deben cargar correctamente.
- Las rutas deben funcionar también en GitHub Pages.

---

# Formativa 02
## ¿Qué vamos a evaluar?

| Criterio | Puntaje |
|---|---:|
| Navegación entre páginas | 5 pts |
| Página de proyectos | 7 pts |
| Página de contacto | 6 pts |
| Consistencia visual | 4 pts |
| Git y GitHub — mínimo 3 nuevos commits | 5 pts |
| Sitio publicado y funcionando | 3 pts |
| **Total** | **30 pts** |

---

# Parcial
## Sitio web personal final — 40 puntos
**Fecha de entrega: 15 o 16 de septiembre hasta las 23:00 hrs.**

En esta entrega final debemos consolidar y perfeccionar el proyecto de la unidad.

Los objetivos principales de la entrega parcial son:

- **Incorporar la librería de animaciones AOS** en el sitio.
- **Corregir y mejorar las entregas anteriores** (Formativa 01 y Formativa 02) basándose en la retroalimentación recibida.
- Publicar la versión final del sitio web de forma óptima.

---

# HTML semántico

En la entrega final comenzaremos a preocuparnos por la estructura del documento.

Cuando corresponda, utilizaremos elementos como:

- `header`
- `nav`
- `main`
- `section`
- `article`
- `footer`

La idea es utilizar HTML para representar la **estructura y significado del contenido**, no solamente llenar todo de `div`.

---

# CSS
## Personaliza tu sitio

El layout entregado por la profesora es una **referencia**, no un diseño obligatorio.

Puedes modificar:

- colores,
- tipografía,
- imágenes,
- bordes,
- tamaños,
- espacios,
- alineación,
- distribución de los elementos.

La versión final debe demostrar decisiones visuales propias.

Los **colores y tipografías son de libre elección**, pero debe mantenerse el layout general basado en un **contenedor o cuadrado central**.

---

# Interacción con CSS

Nuestro sitio también puede reaccionar a algunas acciones del usuario sin utilizar JavaScript.

Por ejemplo:

```css
a:hover {
  opacity: 0.7;
}
```

La entrega final debe incorporar al menos estados visuales para enlaces o botones mediante CSS.

---


# Librería de animaciones
## AOS — Animate On Scroll

En la entrega final se deberá utilizar la librería **AOS (Animate On Scroll)**.

AOS permite agregar animaciones utilizando atributos directamente en nuestros elementos HTML.

Ejemplo:

```html
<section data-aos="fade-up">
  Contenido
</section>
```

Se pueden utilizar animaciones como:

```html
data-aos="fade-up"
data-aos="fade-right"
data-aos="fade-left"
data-aos="zoom-in"
data-aos="flip-left"
```

### Requisito

- Utilizar AOS en al menos **3 elementos del sitio**.
- Las animaciones deben funcionar correctamente.
- Deben utilizarse de manera coherente.
- No deben dificultar la lectura ni la navegación.
- No es necesario crear animaciones propias con JavaScript.

---

# Responsive
## ¿Qué pasa cuando achicamos la pantalla?

Nuestro sitio debe poder visualizarse correctamente tanto en:

### Desktop 🖥️

como en:

### Mobile 📱

El **contenedor o cuadrado central también debe ser responsive**.

En desktop puede mantener una proporción amplia y centrada. En pantallas pequeñas debe reducir su ancho y adaptarse al espacio disponible sin provocar scroll horizontal ni contenido cortado.

No buscamos crear una interfaz compleja.

Buscamos evitar que nuestro sitio **explote cuando cambia el tamaño de la pantalla**.

---

# Responsive
## ¿Qué debemos revisar?

En pantallas pequeñas:

- El contenido no debe salir de la pantalla.
- Los textos deben continuar siendo legibles.
- Las imágenes deben adaptarse.
- Los proyectos pueden pasar de columnas a filas.
- La navegación debe continuar siendo utilizable.
- El formulario debe adaptarse al ancho disponible.
- El contenedor central debe disminuir su ancho de forma proporcional.
- El contenedor debe mantener márgenes laterales suficientes en mobile.
- No debe existir scroll horizontal causado por el layout.

Podemos utilizar `@media`, porcentajes, `max-width` y otras propiedades CSS para adaptar nuestro diseño.

---

# Organización del proyecto

La entrega final debe mantener los archivos ordenados.

Ejemplo:

```text
mi-sitio/
│
├── index.html
├── proyectos.html
├── contacto.html
│
├── css/
│   └── style.css
│
└── img/
    ├── perfil.jpg
    ├── proyecto-01.jpg
    ├── proyecto-02.jpg
    └── proyecto-03.jpg
```

---

# Imágenes y accesibilidad básica

Las imágenes deben:

- cargar correctamente,
- mantener tamaños adecuados,
- no deformarse,
- incorporar atributo `alt` cuando corresponda.

Ejemplo:

```html
<img src="img/perfil.jpg" alt="Fotografía de perfil">
```

---

# Git también es parte del proyecto

No queremos esto:

```text
commit 1: tarea
commit 2: tarea2
commit 3: listo
```

Queremos que el historial nos permita entender el proceso.

Por ejemplo:

```text
crea estructura página proyectos
agrega formulario de contacto
corrige navegación mobile
```

Los commits representan **momentos del desarrollo**.

---

# Parcial
## ¿Qué vamos a evaluar?

| Criterio | Puntaje |
|---|---:|
| Estructura y contenido HTML | 8 pts |
| CSS y presentación visual | 5 pts |
| Navegación y funcionamiento | 6 pts |
| Responsive del layout central | 5 pts |
| Librería AOS | 3 pts |
| Mejoras respecto a las formativas | 4 pts |
| Git y proceso de trabajo | 5 pts |
| Publicación final | 4 pts |
| **Total** | **40 pts** |

---

# Entrega final
## Checklist

Antes de entregar verifica:

- [ ] Inicio funciona.
- [ ] Proyectos funciona.
- [ ] Contacto funciona.
- [ ] La navegación conecta las 3 páginas.
- [ ] Existen 3 proyectos.
- [ ] Las imágenes cargan.
- [ ] El formulario está construido correctamente.
- [ ] El CSS está vinculado.
- [ ] El sitio funciona en desktop.
- [ ] El sitio funciona en mobile.
- [ ] El contenedor central se adapta correctamente al ancho de pantalla.
- [ ] No existe scroll horizontal provocado por el layout.
- [ ] Utilicé AOS en mínimo 3 elementos.
- [ ] Las animaciones funcionan correctamente.
- [ ] El repositorio está actualizado.
- [ ] Realicé mínimo 3 nuevos commits.
- [ ] GitHub Pages está publicado.

---

# Rúbrica completa
## Formativa 01 — 30 puntos

| Criterio | Logro completo | Logro parcial | Logro insuficiente | Máx. |
|---|---|---|---|---:|
| **Estructura HTML** | Documento HTML5 correctamente construido, organizado y con los elementos solicitados. | Presenta la estructura principal, pero existen errores menores o elementos mal utilizados. | Estructura incompleta, errores importantes o contenido sin organizar correctamente. | **8** |
| **Card de presentación** | Incluye imagen/avatar, nombre, descripción, especialidad/intereses y mínimo 2 enlaces funcionales. | Incluye la mayoría de los elementos, pero falta información o existen enlaces sin funcionar. | Card incompleta o no permite identificar claramente la presentación personal. | **8** |
| **CSS y presentación visual** | Utiliza CSS externo y evidencia trabajo en colores, tipografía, espacios, tamaños y alineación. | Utiliza CSS, pero la personalización o distribución es limitada o presenta problemas menores. | CSS ausente, mal vinculado o con problemas que afectan significativamente la presentación. | **6** |
| **Git y GitHub** | Repositorio actualizado, mínimo 3 commits que evidencian avances reales y mensajes comprensibles. | Existen commits, pero son insuficientes o no representan claramente el proceso. | No existe historial suficiente o el proyecto no está correctamente almacenado en GitHub. | **5** |
| **GitHub Pages** | Sitio publicado y accesible mediante URL pública. | Sitio publicado con errores menores. | Sitio no publicado o inaccesible. | **3** |
| | | | **TOTAL** | **30** |

---

# Rúbrica completa
## Formativa 02 — 30 puntos

| Criterio | Logro completo | Logro parcial | Logro insuficiente | Máx. |
|---|---|---|---|---:|
| **Navegación** | Inicio, Proyectos y Contacto están correctamente conectados y todos los enlaces internos funcionan. | La navegación existe, pero presenta uno o más errores de rutas o consistencia. | No existe navegación funcional entre las páginas. | **5** |
| **Página de proyectos** | Presenta 3 proyectos con nombre, descripción e imagen correctamente organizados. | Presenta los proyectos, pero existen elementos incompletos, imágenes faltantes o problemas de organización. | Faltan proyectos o la página está significativamente incompleta. | **7** |
| **Página de contacto** | Formulario con labels, campos apropiados, textarea, botón y atributos HTML solicitados. | Formulario funcional visualmente, pero presenta campos o atributos incompletos. | Formulario incompleto o construido con elementos HTML inadecuados. | **6** |
| **Consistencia visual** | Las tres páginas mantienen navegación, tipografía, colores, espacios y estilos coherentes. | Existe cierta consistencia, pero algunas páginas presentan diferencias importantes. | Las páginas parecen proyectos independientes o el CSS presenta problemas significativos. | **4** |
| **Git y GitHub** | Mínimo 3 nuevos commits que evidencian la construcción progresiva del sitio. | Existen commits nuevos, pero son insuficientes o poco descriptivos. | No se evidencia proceso de trabajo mediante Git. | **5** |
| **Publicación** | Las 3 páginas funcionan correctamente desde GitHub Pages, incluyendo estilos, imágenes y navegación. | El sitio está publicado, pero presenta errores menores. | El sitio no está publicado o presenta errores que impiden navegarlo. | **3** |
| | | | **TOTAL** | **30** |

---

# Rúbrica completa
## Parcial — 40 puntos

| Criterio | Logro completo | Logro parcial | Logro insuficiente | Máx. |
|---|---|---|---|---:|
| **Estructura y contenido HTML** | Las 3 páginas presentan contenido completo, organizado y utilizan correctamente elementos HTML, incluyendo semántica cuando corresponde. | El contenido está mayormente completo, pero existen errores estructurales o semánticos menores. | Existen problemas importantes de estructura, contenido incompleto o uso incorrecto de HTML. | **8** |
| **CSS y presentación visual** | Sitio personalizado, legible y coherente. Los colores y tipografías son de libre elección, pero se mantiene correctamente el layout central solicitado. | El sitio posee estilos propios, pero presenta inconsistencias visuales o se aleja parcialmente del layout solicitado. | CSS incompleto, poco trabajado o no mantiene correctamente la estructura visual requerida. | **5** |
| **Navegación y funcionamiento** | Navegación, enlaces, imágenes, formulario y rutas funcionan correctamente en todo el sitio. | El sitio funciona, pero presenta algunos enlaces, imágenes o rutas con errores. | Existen errores importantes que impiden recorrer o utilizar el sitio correctamente. | **6** |
| **Responsive del layout central** | El contenedor central y su contenido se adaptan correctamente a desktop y mobile, sin scroll horizontal, desbordes ni contenido ilegible. | Existe adaptación responsive, pero el contenedor o algunos elementos presentan problemas en ciertos tamaños. | El contenedor central no es responsive o la versión mobile presenta desbordes y problemas importantes. | **5** |
| **Librería AOS** | Se utiliza AOS correctamente en al menos 3 elementos, con animaciones coherentes que aportan a la experiencia sin dificultar la navegación. | Se utiliza AOS, pero existen errores menores, pocas animaciones funcionales o uso poco consistente. | AOS no está incorporado, no funciona o su uso afecta negativamente la experiencia. | **3** |
| **Mejoras respecto a las formativas** | Se evidencian correcciones, mejoras y aplicación del feedback recibido durante el proceso. | Se incorporan algunas mejoras, pero permanecen problemas detectados anteriormente. | No se evidencian mejoras relevantes respecto de las entregas anteriores. | **4** |
| **Git y proceso de trabajo** | Mínimo 3 nuevos commits descriptivos que permiten observar claramente el proceso de mejora y cierre. | Existen commits, pero son insuficientes, concentrados al final o poco descriptivos. | No se evidencia adecuadamente el proceso mediante Git. | **5** |
| **Publicación final** | Versión final correctamente publicada en GitHub Pages, sin errores importantes de carga o rutas. | Publicación disponible con errores menores. | Sitio no publicado o con errores graves que impiden su revisión. | **4** |
| | | | **TOTAL** | **40** |

---

# Resultado final

### Formativa 01
**30 puntos**
*Entrega: miércoles 2 de septiembre a las 23:00 hrs.*

### Formativa 02
**30 puntos**
*Entrega: miércoles 9 de septiembre a las 23:00 hrs.*

### Parcial
**40 puntos**
*Entrega: 15 o 16 de septiembre hasta las 23:00 hrs.*

# 100 puntos

Al terminar tendrás un sitio web personal construido desde cero utilizando **HTML + CSS + AOS + Git + GitHub**.
