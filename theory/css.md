# CSS

**CSS (Cascading Style Sheets)** es el lenguaje que se utiliza para describir la presentación de documentos HTML. Controla el diseño visual: colores, fuentes, espaciado, disposición, animaciones, etc.

---

## 2. Tipos de CSS

- **Inline CSS**: en la etiqueta HTML.  
  Ej: `<p style="color: red;">Texto</p>`

- **Internal CSS**: dentro del `<style>` en el `<head>`.

- **External CSS**: en un archivo `.css` vinculado con `<link>` (el más recomendado).

---

## 3. Selectores

### 🔹 Básicos

- `*`: todos los elementos

- `elemento`: todos los elementos de ese tipo (`p`, `div`, etc.)

- `.clase`: elementos con esa clase

- `#id`: elemento con ese ID

- `elemento1, elemento2`: varios selectores

### 🔹 Combinadores

- `elemento elemento`: descendiente

- `elemento > hijo`: hijo directo

- `elemento + hermano`: hermano siguiente inmediato

- `elemento ~ hermano`: todos los hermanos siguientes

### 🔹 Pseudoclases

- `:hover`: al pasar el mouse

- `:focus`: cuando está enfocado (input)

- `:nth-child(n)`, `:first-child`, `:last-child`

- `:not(selector)`: niega un selector

### 🔹 Pseudoelementos

- `::before` y `::after`: contenido generado

- `::first-line`, `::first-letter`

---

## 4. Especificidad y Cascada

- Regla de oro: **más específico = más prioridad**.

- Orden de prioridad (mayor a menor):

  1. Estilo inline
  2. ID (`#id`)
  3. Clase, pseudoclase, atributo
  4. Elemento y pseudoelemento

- La **cascada** se refiere al orden de carga: últimas reglas sobreescriben anteriores si tienen la misma especificidad.

---

## 5. Unidades

- **Relativas**:

  - `em`: relativo al `font-size` del padre

  - `rem`: relativo al `font-size` del `html`

  - `%`: relativo al contenedor

  - `vh`, `vw`: relativo a viewport height/width

- **Absolutas**:

  - `px`: píxeles (más común)

  - `pt`, `cm`, `in`: impresión

---

## 6. Modelo de Caja (Box Model)

Cada elemento tiene:

- `content`: contenido

- `padding`: espacio interno

- `border`: borde

- `margin`: espacio externo

```css
box-sizing: content-box; /* valor por defecto */
box-sizing: border-box; /* recomendado */
```

---

## 7. Propiedades Comunes

### 🖌️ Textos

```css
color, font-size, font-family, font-weight, line-height, text-align, text-transform, letter-spacing, word-spacing
```

### Tamaño y Espaciado

```css
width, height, max-width, min-height, margin, padding
```

### Bordes y Fondo

```css
border, border-radius, background-color, background-image, background-size, background-position
```

### Display y Posicionamiento

```css
display: block | inline | inline-block | flex | grid | none;
position: static | relative | absolute | fixed | sticky;
top, right, bottom, left, z-index
```

---

## 8. Flexbox

Sistema de diseño unidimensional.

### Contenedor

```css
display: flex;
flex-direction: row | column;
justify-content: start | center | space-between;
align-items: stretch | center | baseline;
gap: 1rem;
```

### Ítems

```css
flex-grow, flex-shrink, flex-basis, align-self, order
```

---

## 9. Grid

Sistema de diseño bidimensional.

### Contenedor Flex

```css
display: grid;
grid-template-columns: 1fr 2fr;
grid-template-rows: 100px auto;
gap: 10px;
```

### Ítems Flex

```css
grid-column: 1 / 3;
grid-row: 2 / 4;
grid-area: header;
```

---

## 10. Responsive Design

### Media Queries

```css
@media (max-width: 768px) {
  /* estilos para móviles */
}
```

### Técnicas

- Layouts fluidos (`%`, `vw`)

- Flexbox / Grid

- `clamp()`, `min()`, `max()`

- Unidades relativas (`em`, `rem`)

---

## 11. Colores

- Nombres: `red`, `blue`

- Hex: `#ff0000`

- RGB: `rgb(255, 0, 0)`

- RGBA: `rgba(255, 0, 0, 0.5)`

- HSL: `hsl(0, 100%, 50%)`

---

## 12. Transiciones y Animaciones

### Transiciones

```css
transition: property duration ease delay;
```

### Animaciones

```css
@keyframes ejemplo {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
animation: ejemplo 2s infinite;
```

---

## 13. Herramientas y Buenas Prácticas

- Usar `normalize.css` o `reset.css`

- Prefijos: `-webkit-`, `-moz-`, etc. (cada vez menos necesarios)

- Nombres de clases con metodología **BEM**

- Modularización de archivos `.css`

- Organización por componentes si usas frameworks

---

## 14. Herramientas Modernas

- **Preprocesadores**: Sass, Less

- **Postprocesadores**: PostCSS

- **Frameworks CSS**: Tailwind CSS, Bootstrap

- **Autoprefixer**, **CSS Modules**, **Styled Components**

---

## 15. Buenas Prácticas

- Mantén el CSS limpio y organizado

- Reutiliza clases

- Usa variables CSS (`--primary-color`) para mantener consistencia

- Agrupa por componentes o secciones

- Elimina código no usado
