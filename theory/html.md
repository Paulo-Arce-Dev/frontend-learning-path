# HTML

- **HyperText Markup Language**
- Nos permite indicar la estructura de nuestra página mediante etiquetas (describir el contenido).
- Tiene gran adaptabilidad.
- Estructuración lógica.
- Fácil de interpretar para humanos y máquina.
- No se ocupa de la presentación (como se ve, ese es CSS).
- De la interactividad se encarga JavaScript.
- Con las etiquetas creamos elementos (nodos).

## Tipos de elementos HTML

- **Normales**
- **Reemplazables**: normalmente sin etiqueta de cierre, reemplazables por contenido multimedia, etc. (como `<img>`, `<input>`).

---

## 🏷️ Etiquetas principales

- `<!DOCTYPE html>` – Indica que es un documento HTML.
- `<html>` – Define el inicio y el final de la página web.
- `<head>` – Información para el navegador (SEO, favicon, meta datos).
- `<title>` – Título que aparece en la pestaña del navegador.
- `<body>` – Cuerpo visible de la página.

## Texto y estructura

- `<h1>` a `<h6>` – Encabezados.
- `<p>` – Párrafo.
- `<strong>` – Énfasis fuerte (negrita).
- `<b>` – Negrita (no semántica).
- `<em>` – Énfasis.

## Listas

- `<ul>` – Lista desordenada.
- `<ol>` – Lista ordenada.
- `<li>` – Elemento de lista.
- `<dl>` – Lista de descripciones.
- `<dt>` – Término.
- `<dd>` – Definición.

## Texto especial y semántico

- `<abbr>` – Abreviatura.
- `<address>` – Información de contacto.
- `<bdo>` – Dirección del texto.
- `<blockquote>` – Cita de otra fuente.
- `<cite>` – Título de obra.
- `<q>` – Cita en línea.
- `<code>` – Fragmento de código.
- `<ins>` – Texto insertado.
- `<del>` – Texto eliminado.
- `<dfn>` – Definición.
- `<kbd>` – Entrada por teclado.
- `<pre>` – Texto preformateado.
- `<samp>` – Salida de programa.
- `<var>` – Variable.
- `<br>` – Salto de línea.
- `<div>` – División general.

## Multimedia y enlaces

- `<a>` – Enlace.
- `<base>` – URL base para enlaces relativos.
- `<img>` – Imagen.
- `<area>` – Área de un mapa de imagen.
- `<map>` – Mapa de imagen.
- `<param>` – Parámetro para `<object>`.
- `<object>` – Insertar objeto.

## Formularios e inputs

- `<input>` – Muchos tipos:
  - `text`, `password`, `checkbox`, `radio`, `submit`, `reset`, `button`
  - `email`, `tel`, `number`, `search`, `url`, `file`, `color`, `range`
  - `date`, `month`, `week`, `time`, `datetime`, `datetime-local`
  - `image`, `hidden`

---

## 🔧 Atributos

- Proporcionan **información adicional** a los elementos HTML.
- **Tipos**:
  - **Globales**: Se pueden usar en cualquier etiqueta (`class`, `id`, `style`, `lang`, etc).
  - **Específicos**: Solo para ciertas etiquetas (`src`, `alt`, `href`, etc).
- Las comillas son **opcionales**, excepto para cadenas de texto con espacios.
- **Booleanos**: Se consideran verdaderos si están presentes (ej: `hidden`, `checked`, `disabled`).

### Atributos comunes

- `alt`, `src`, `title`, `class`, `id`
- `onClick`, `style`, `width`, `height`, `target`, `href`, `lang`
- `disabled`, `checked`

---

## 🧩 HTML Semántico

HTML semántico **describe el contenido de forma más clara y estructurada**.

- ❌ Error típico: usar muchos `<div>` sin sentido semántico.
- ✅ Usar etiquetas específicas según el contenido.

### Ejemplos de etiquetas semánticas

- `<header>` – Encabezado principal o de sección.
- `<main>` – Contenido principal de la página.
- `<section>` – Sección de contenido relacionada.
- `<article>` – Contenido independiente que tiene sentido por sí mismo.
- `<aside>` – Contenido secundario o complementario.
- `<footer>` – Pie de página.
- `<nav>` – Navegación principal.
- `<small>` – Texto de menor importancia (ej: copyright).
- `<a>` – Navegar internamente o externamente.
- `role` – Mejora la accesibilidad indicando el rol del elemento.

---

## 📝 Notas

> ⚠️ Los botones dentro de un `<form>` son de tipo `submit` por defecto.  
> ⚠️ No usar `loading="lazy"` en imágenes muy arriba en la página.
