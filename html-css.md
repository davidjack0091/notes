**html** - structure of webpage
**css** - appearance of webpage
**javascript** - behaviour of webpage

# html

html reference

**element** - opening tag + content + closing tag
**void element** - element without content and closing tag.
**attribute** - additional information about element.

**semantic element** - provide information about their content.
`<header>`, `<article>`, `<nav>`, etc.
**non semantic element** - provide no information about their content. for styling and layout.
`<div>`, `<span>`, etc.

### vs code - (! + enter)
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
    </head>
    <body></body>
</html>
```
### main root
`<html>` -> `lang`

### document metadata
`<head>`
=> `<meta />` -> `charset="UTF-8"`
=> `<meta />` -> `name="viewport"`, `content="width=device-width`, `initial-scale=1.0"` (responsive)
=> `<title>`
=> `<style>` (internal css)
=> `<script>` (internal javascript)
=> `<link />` -> `href="style.css"`, `rel="stylesheet"` (external css)
=> `<script>` -> `src="script.js"`, `defer` (external javascript)

### sectioning root
`<body>`

### content sectioning
`<address>`, `<article>`, `<aside>`, `<main>`, `<nav>`, `<section>`, `<header>`, `<footer>`
`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`

### text content
`<p>`, `<blockquote>`, `<pre>`, `<hr />`
`<dl>`
=> `<dt>`
=> `<dd>`
`<ol>`
=> `<li>`
=> `<ul>`
`<figure>`
=> `<img />`
=> `<figcaption>`
`<div>` (block container)

inline text semantics
<a> -> href="https://example.com", target="_self(dafault)/_blank/_parent/_top"
    -> rel="noopener/noreferrer" (if target="_blank")
<q>, <br />, <b>, <i>, <em>, <strong>
<span> (inline container)

image and multimedia
<img /> -> src="image.jpg", alt

embedded content
<picture> (responsive) => <source /> -> srcset="image-one.jpg"
                       => <img />

table content
<table> => <caption>
        => <colgroup> => <col> -> span
        => <thead> => <tr> => <th> -> scope="col/row", colspan/rowspan
        => <tbody> => <tr> => <th> -> scope="col/row", colspan/rowspan
                           => <td> -> colspan/rowspan
        => <tfoot> => <tr> => <th> -> scope="col/row", colspan/rowspan
                           => <td> -> colspan/rowspan

forms
<form> -> action
       -> method (get/post)
       -> target="_self(dafault)/_blank/_parent/_top"
          don't use action, method, target - if handling form submission using javascript
       -> enctype="application/x-www-form-urlencoded" (default)
                  "multipart/form-data" (if <input type="file">)
                  "text/plain"
       -> novalidate (form validation)

<label> -> for (id of <input>)
<input /> -> type="checkbox/date/email/file/hidden/image/month/number/
                   password/radio/search/tel/text/time/url/week"
          -> value (for checkbox, radio, hidden)
          -> id, name, placeholder, disabled, readonly, multiple
          -> required, min, max, minlength, maxlength, size, pattern (form validation)

<fieldset> => <legend>
           => <label>
           => <input />

<select> => <optgroup> -> label
         => <option -> label, selected
<textarea> -> rows, cols

<button> -> type="button/submit/reset"

interactive element
<dialog> -> open

global attribute
id, class, hidden, title
tabindex
style (inline css)
data-* (to store your own custom data on elements and read it later in javascript using dataset property)

svg
<svg>

icons in html
- copy emoji/icons and paste
- svg file in <img>
- icon fonts (font awesome, material icons, etc)
- inline <svg>
icons in css
- background-image property
- ::before/::after pseudo element

css

css reference

selectors - element to which css rules apply.

basic selector
* {...}       - universal selector
element {...} - type selector
#id {...}     - id selector
.class {...}  - class selector - prefer

attribute selector
element[attribute] {...}
element[attribute="value"] {...}
element[attribute^="value"] {...}
element[attribute$="value"] {...}
element[attribute*="value"] {...}

chaining selector
.class1.class2 {...}
element.class {...}
element#id {...}
.class#id {...}
id.class {...}
.class1.class2.class3 {...}
element.class1.class2 {...}
#id.class1.class2 {...}

combinator
selector1, selector2, ... {...} - selector list
selector1 selector2 {...}       - descendant combinator
selector1 > selector2 {...}     - child combinator - selector2 is direct child of selector1
selector1 + selector2 {...}     - next sibling combinator
selector1 ~ selector2 {...}     - subsequent sibling combinator

pseudo class - a keyword added to a selector to style a specific state of selected element.
:root
:focus
:hover
:active
:link
:visited
:empty
:first-child
:last-child
:only-child
:nth-child


form validation
:valid
:invalid

pseudo element - a keyword added to a selector to style a specific part of selected element.
::marker
::first-letter
::first-line
::selection
::before
::after

css rules
cascade - determines which css rules wins when multiple css rules apply to same element.
specificity - when multiple selectors applied css rules to same element.
1. inline css > internal css, external css
2. id selector > class selector > type selector
3. more number of selector > less number of selector
- chaining selector = descendant combinator
- no specificity - child combinator, next sibling combinator, subsequent sibling combinator, 
                   universal selector
inheritance - some properties when applied to elements are inherited by child elements even if you don't write css rules for them.
- child selector > parent selector
rule order - if everything (specificity + inheritance) is equal.
- last defined css rules will be applied.

text/font

fonts
font: value - shorthand
font-family: value
font-size: value
font-style: value
font-weight: value

inline layout
line-height: value

text
letter-spacing: value
text-align: value
text-wrap: value
text-transform: value
white-space: value

text decoration
text-decoration: value
text-shadow: value

inline layout
line-height: value

overflow
overflow: value - shorthand
overflow-x: value
overflow-y: value

text-overflow: value

background/border/color

backgrounds and borders
background: value - shorthand
background-color: value - use custom property instead
background-image: value
background-size: "cover" - responsive
background-position = "center" - responsive

border: value - shorthand
border-width: value - shorthand
border-style: value - shorthand
border-color: value - shorthand

border-radius: value - shorthand
box-shadow: value

* { border: 1px solid red } - debug

basic user interface
outline: value - shorthand
outline-color: value
outline-style: value
outline-width: value

cursor: value
resize: value

colors
color: value - use custom property instead
opacity: value
rgb(): value
hsl(): value
#hex

layout 1

box model - every element in a webpage is a rectangular box.
properties - margin, padding, border, height, width.

responsive
margin: value - shorthand
margin-top: value
margin-right: value
margin-bottom: value
margin-left: value

responsive
padding: value - shorthand
padding-top: value
padding-right: value
padding-bottom: value
padding-left: value

center a block element
width/max-width: value
margin: 0 auto

box sizing
box-sizing: "border-box"

- responsive
*,
*::before,
*::after {  
    box-sizing: "border-box";  margin: 0;  padding: 0;
}

height: value
width: value
- element is same size for all screen size - content can overflow
- logo, icon, button, sidebar, fixed image, etc
.icon {  width: 18px; height: 18px  }
img {  width: 300px; height: auto  }
height: auto (except header, footer, etc.) - responsive
width/height: 70% - responsive


max-height: value - responsive
max-width: value - responsive
min-height: value - responsive
min-width: value - responsive
- element can adjust size according to screen size
- responsive container, responsive image, anything that should adapt to screen size
img {  max-width: 100%; height: auto  }
.container {  width: 100%; max-width: 1200px  }

aspect-ratio: value - responsive

positioned layout
position: value - don't use absolute value - responsive
top: value
right: value
bottom: value
left: value
z-index: value

layout 2
display - how element is displayed (block or inline) and how its children are arranged.
block - element is block container and children follow block layout.
inline-block - element is inline container and children follow block layout.
flex - element is block container (flex container) and children (flex items) follow flex layout.
     - arranging items in one direction (rows or columns).
inline-flex - element is inline container and children follow flex layout.
grid - element is block container (grid container) and children (grid items) follow grid layout.
     - arranging items in both directions (rows and columns).
inline-grid - element is inline container and children follow grid layout.

visibility: value

- container property
display: "block/inline-block/flex/inline-flex/grid/inline-grid/none" - flex/grid - responsive


- items property
order: value

flexible box layout (flex layout) - after setting display to flex/inline-flex.
main axis - direction of flow of flex items
cross axis - perpendicular to main axis

- container property
flex-flow: value - shorthand
flex-direction: value
flex-wrap: "wrap" - responsive


- items property
flex: value - shorthand
flex-grow: value
flex-shrink: value
flex-basis: value

grid layout - after setting display to grid.
block axis - rows
inline axis - columns

- container property
grid-template-areas: value
grid-template-columns: value
grid-template-rows: value


- items property
grid-column: value - shorthand
grid-row: value - shorthand

- responsive
repeat()
minmax()
fr

box alignment - after setting display to flex/grid.
- container property
align-content: value
align-items: value
justify-content: value
justify-items: value - not work in flex layout
gap: value - shorthand
column-gap: value
row-gap: value


- items property
align-self: value
justify-self: value - not work in flex layout

units

values and units
auto - responsive
absolute unit - cm, in, px
relative unit - responsive - percentage of parent element
%, rem - fonts, vh, vw - section height

url()
calc()
clamp()
responsive  min(), max()

advance concepts

animations
animation: value - shorthand
animation-delay: value
animation-direction: value
animation-duration: value
animation-fill-mode: value
animation-iteration-count: value
animation-name: value
animation-play-state: value
animation-timing-function: value

transforms
perspective: value
rotate: value
scale: value
transform: value
translate: value

matrix/3d(): value
perspective(): value
rotate/X/Y/Z/3d(): value
scale/X/Y/Z/3d(): value
skew/X/Y(): value
translate/X/Y/Z/3d(): value

transitions
transition: value - shorthand
transition-delay: value
transition-duration: value
transition-property: value
transition-timing-function: value

images
object-fit: "cover" - responsive

linear-gradient(): value

generated content
content: value

filter effects
filter: value

custom properties for cascading variables
--
var()

:root {
    --first-color: #1166ff;
    --second-color: #ffff77;
}
.firstParagraph {
    background-color: var(--first-color);
    color: var(--second-color);
}
.container {
    --first-color: #229900;
}

at-rules

media queries - make a website responsive by applying different css rules based on device characteristics such as screen size, resolution, orientation, user preferences (color scheme).

@media
prefers-color-scheme

responsive design/layout
- websites should respond to changes in browser size or screen on any device.
- most of elements are responsive until you change them in css.
- if you mostly use natural responsiveness then you don't need much extra things to do to make websites responsive.

breakpoints - if layout breaks anywhere between 320px and 1400px then it's not responsive.
- check on mobile, tablet, laptop, portrait/landscape, zoom 100% to 175%
mobile - <600px
tablet - 600px-1200px
laptop - >1200px
@media (max-width: 600px) {
    - fix stuff here
}

bootstrap

tailwind

sass

javascript


