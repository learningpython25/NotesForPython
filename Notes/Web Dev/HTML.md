
* **HTML (HyperText Markup Language)** is the standard language used to create webpages.
* It structures content using **elements** (tags) like `<p>`, `<div>`, `<a>`, etc.

---

## 🔤 2. Basic Structure

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Main Heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

---

## 📦 3. Common Tags

| Tag             | Purpose                       |
| --------------- | ----------------------------- |
| `<h1>` – `<h6>` | Headings (1 = most important) |
| `<p>`           | Paragraph                     |
| `<a>`           | Hyperlink                     |
| `<img>`         | Image                         |
| `<div>`         | Generic container             |
| `<span>`        | Inline container              |
| `<br>`          | Line break                    |
| `<hr>`          | Horizontal rule               |

---

## 🧩 4. Attributes

```html
<img src="image.png" alt="Description" width="200" height="100">
```

| Attribute | Description                      |
| --------- | -------------------------------- |
| `src`     | Image or resource source         |
| `href`    | Link destination (used in `<a>`) |
| `alt`     | Alt text for images              |
| `id`      | Unique identifier                |
| `class`   | Reusable CSS class               |
| `style`   | Inline styling                   |

---

## 🔗 5. Links

```html
<a href="https://example.com" target="_blank">Visit Site</a>
```

* `target="_blank"` opens in a new tab.

---

## 🖼 6. Images

```html
<img src="pic.jpg" alt="A picture" />
```

---

## 📝 7. Forms & Inputs

```html
<form action="/submit" method="POST">
  <input type="text" name="username" />
  <input type="password" name="password" />
  <input type="submit" value="Login" />
</form>
```

Common input types:

* `text`, `password`, `email`, `checkbox`, `radio`, `submit`, `file`, `date`

---

## 🧮 8. Semantic Elements

Semantic tags describe meaning:

* `<header>`, `<footer>`, `<article>`, `<section>`, `<nav>`, `<main>`, `<aside>`

Helps with SEO and accessibility.

---

## ⚙️ 9. Block vs Inline Elements

| Type   | Examples                    | Behavior             |
| ------ | --------------------------- | -------------------- |
| Block  | `<div>`, `<p>`, `<section>` | Starts on a new line |
| Inline | `<span>`, `<a>`, `<img>`    | Flows within text    |

---

## 🎨 10. HTML + CSS

Use `<style>` or external CSS to style HTML:

```html
<style>
  p { color: red; font-size: 16px; }
</style>
```

Or link to a CSS file:

```html
<link rel="stylesheet" href="style.css">
```
