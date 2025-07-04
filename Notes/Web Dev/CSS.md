* **CSS (Cascading Style Sheets)** is used to style and layout HTML elements.
* Controls **color**, **font**, **size**, **position**, and more.

---

## 📌 2. Ways to Apply CSS

```html
<!-- Inline -->
<p style="color: red;">Text</p>

<!-- Internal -->
<style>
  p { color: red; }
</style>

<!-- External -->
<link rel="stylesheet" href="styles.css">
```

---

## 🔍 3. Selectors

| Selector   | Example   | Description                      |
| ---------- | --------- | -------------------------------- |
| Universal  | `*`       | Selects all elements             |
| Element    | `p`, `h1` | Selects all `<p>`, `<h1>` etc.   |
| Class      | `.box`    | Selects all with `class="box"`   |
| ID         | `#main`   | Selects element with `id="main"` |
| Grouping   | `h1, h2`  | Applies to both h1 and h2        |
| Descendant | `div p`   | `<p>` inside `<div>`             |
| Child      | `div > p` | Direct child `<p>` of `<div>`    |

---

## 🎛 4. Box Model

```txt
[ margin ]
  [ border ]
    [ padding ]
      [ content ]
```

| Property       | Description                  |
| -------------- | ---------------------------- |
| `margin`       | Space **outside** the border |
| `border`       | Border around padding        |
| `padding`      | Space **inside** the border  |
| `width/height` | Size of the content area     |

---

## 🎨 5. Common Properties

```css
color: blue;
background-color: yellow;
font-size: 16px;
font-family: Arial, sans-serif;
text-align: center;
margin: 10px;
padding: 5px;
border: 1px solid black;
```

---

## 📐 6. Units

| Unit      | Meaning                 |
| --------- | ----------------------- |
| `px`      | Pixels                  |
| `%`       | Percentage              |
| `em`      | Relative to parent font |
| `rem`     | Relative to root font   |
| `vh`/`vw` | Viewport height/width   |

---

## 📦 7. Display & Position

### `display`

* `block`, `inline`, `inline-block`, `none`, `flex`, `grid`

### `position`

* `static`, `relative`, `absolute`, `fixed`, `sticky`

```css
position: absolute;
top: 10px;
left: 20px;
```

---

## 🧭 8. Flexbox (Layout)

```css
display: flex;
justify-content: space-between;
align-items: center;
```

Common values:

* `justify-content`: `center`, `space-between`, `space-around`
* `align-items`: `center`, `flex-start`, `flex-end`

---

## 📊 9. Grid (Layout)

```css
display: grid;
grid-template-columns: 1fr 2fr;
grid-gap: 10px;
```

---

## 🔁 10. Pseudo-Classes & Pseudo-Elements

```css
a:hover { color: red; }
p::first-line { font-weight: bold; }
```

| Type           | Syntax     | Purpose                       |
| -------------- | ---------- | ----------------------------- |
| Pseudo-class   | `:hover`   | State-based styling           |
| Pseudo-element | `::before` | Insert content or style parts |

---
## 🌈 11. Media Queries (Responsive Design)

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```
