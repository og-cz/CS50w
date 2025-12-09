# Web Programming

# HTML

Hypertext markup language - is the standard markup language used to create and structure content on the web

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello!</title>
</head>
<body>
    Hello, World!
</body>
</html>
```

- <!DOCTYPE html> → doctype declaration, this specifies which html version we are using
- <html lang="en"> → html tags, specifies the start of the html page and lang attribute tells what language it was written it too
- <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello!</title>
</head>  → head is a container for metadata and other information that is not directly displayed on the webpage but is essential for the document's functionality and presentation.
- <body>
    Hello, World!
</body> → body tag indicates the visible part of the page

### Document Object Model

The (DOM) is a programming interface for web documents that represents the structure of a document such as HTML, XML, or SVG as a tree of objects in memory.

![image.png](attachment:64770493-98a2-4c8e-9ecd-7ad00eed97a8:image.png)

![image.png](attachment:5ef424bb-a295-4275-af36-4dac23c5fca9:image.png)

# CSS

Cascading Style Sheets, is a style sheet language used to specify the presentation and styling of a document written in a markup language such as HTML or XML.

### CSS styling elements

**Size**

- **width** → sets width
- **height** → sets height
- **padding** → is inside the border margin
- **margin** → is outside the border margin

**Font**

- **font-family** → sets what font to use
- **font-size** → sets size of font
- **font-weight** → sets the font`s “boldness”
- **border** → adds a border in a element

**Table**

- **border** → adds a border in a element
- **border-collapse →** controls how the borders of table cells are rendered, determining whether they are shared between adjacent cells or kept separate.

### CSS Selectors

![image.png](attachment:5a923181-219f-4ebf-8c1b-ac894595bdaf:image.png)

**1. Element Selector**
Selects all elements of a type.

`p { color: red; }` → all `<p>` turn red.

**2. Class Selector**
Selects elements with a class.

`.box { border: 1px solid; }` → `<div class="box">` gets border.

**3. ID Selector**
Selects element with matching ID.

`#main { background: yellow; }` → `<div id="main">` becomes yellow.

**4. Universal Selector**
Selects everything.

- `{ margin: 0; }` → removes margin from all elements.

**5. Descendant Selector (space)**
Selects elements inside another element.

`div p { color: blue; }` → `<p>` inside `<div>` turns blue.

**6. Child Selector (`>`)**
Selects direct children only.

`ul > li { color: green; }` → only immediate `<li>` children turn green.

**7. Adjacent Sibling (`+`)**
Selects the next sibling.

`h1 + p { font-size: 14px; }` → first `<p>` after `<h1>` shrinks.

**8. General Sibling (`~`)**
Selects all following siblings.

`h1 ~ p { color: gray; }` → all `<p>` after `<h1>` turn gray.

**9. Attribute Selector**
Selects based on attributes.

`input[type="text"] { width: 200px; }` → text inputs widen.

**10. Starts With (`^=`)**`a[href^="https"] { color: blue; }` → HTTPS links turn blue.

**11. Ends With (`$=`)**`img[src$=".png"] { border: 1px solid; }` → PNG images get border.

**12. Contains (`*=`)**`[class*="btn"] { padding: 10px; }` → classes containing “btn” get padding.

**13. Pseudo-class**
A special state (hover, focus, etc.).

`button:hover { background: red; }` → button turns red when hovered.

**14. First Child**`li:first-child { font-weight: bold; }` → first `<li>` bold.

**15. Last Child**`li:last-child { color: orange; }` → last `<li>` orange.

**16. Nth Child**`li:nth-child(2) { color: purple; }` → 2nd `<li>` purple.

**17. Pseudo-element ::before**`h1::before { content: "★ "; }` → adds a star before heading.

**18. Pseudo-element ::after**`p::after { content: " END"; }` → adds "END" after paragraph.

**19. Grouping Selector**`.box, p, #main { color: red; }` → all listed selectors turn red.

**20. Not Selector**`:not(.active) { opacity: 0.5; }` → everything not `.active` fades.

## CSS Specificity

```html
<h1 id="foo">Welcome to my Web Page!</h1>

// who will it choose? #foo or h1?
<style>
#foo {
		color: blue;
}

h1 {
		color: red;
}
</style>
```

who will it choose? #foo or h1? the priority it follows is this:

inline → id → class → type

# Responsive Design

### Viewport

The **viewport** is basically the **visible area of a web page on your device’s screen**.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Why it matters (CSS)**

CSS units like:

- `vw` (viewport width)
- `vh` (viewport height)

Are based on the viewport size.

### Media Queries

**Media queries** are a CSS feature that let your webpage **change its style depending on the device** like screen size, orientation, or resolution.

```css
/* Applies only when screen width is 600px or less */
@media (max-width: 600px) {
  body {
    background: lightblue;
  }
}

```

“If the screen is **600px wide or smaller**, then change the body’s background to **light blue**.”

### Flexbox

**Flexbox** is a CSS layout system that makes it easy to arrange items **in a row or column**, and control their spacing, alignment, and size without using floats or complicated hacks.

Think of it like a **smart container** that automatically organizes its children

```css
.container {
  display: flex;
  justify-content: center; /* center horizontally */
  align-items: center;     /* center vertically */
  height: 100vh;
}

```

# Bootstrap

Bootstrap is a CSS framework that gives you ready-made styles and layout tools so you don’t need to write everything from scratch.

**It provides:**

- Pre-styled buttons
- Pre-styled cards
- Grid system (for layout)
- Responsive classes
- Utilities (margin, padding, colors, etc.)

You just **use its classes**.

# Sass

Sass (Syntactically Awesome Style Sheets) is a CSS preprocessor that lets you write cleaner, shorter, and smarter CSS.

Then it compiles into normal CSS that browsers can understand.

Because plain CSS can get messy when:

- You have many files
- You repeat the same colors
- You copy-paste styles
- You want nested styles
- You want functions or logic

Sass fixes all of this.