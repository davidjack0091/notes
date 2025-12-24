# html (structure of webpage)

[html reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference)

**element** - opening tag + content + closing tag  
**void element** - element without content and closing tag.  
**attribute** - additional information about element.

**semantic element** - provide information about their content.  
`<header>` `<article>` `<nav>` etc.  
**non semantic element** - provide no information about their content.  
for styling and layout.  
`<div>` `<span>` etc.

### vs code html boilerplate (! + enter)

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

`<html>`
- `lang` 

### document metadata

`<head>`    
- `<meta />`
     - `charset="UTF-8"`
    - `name="viewport"` `content="width=device-width, initial-scale=1.0"` (responsive)  
- `<title>`  
- `<style>` (internal css)
- `<script>` (internal javascript)  
- `<link />` (external css) 
    - `href="style.css"`
    - `rel="stylesheet"`  
- `<script>` (external javascript)
    - `src="script.js"`
    - `defer`

### sectioning root

`<body>`

### content sectioning

`<address>`  
`<article>`  
`<aside>`  
`<main>`  
`<nav>`  
`<section>`  
`<header>`  
`<footer>`  
`<h1>` `<h2>` `<h3>` `<h4>` `<h5>` `<h6>`

### text content

`<p>`  
`<blockquote>`  
`<pre>`  
`<hr />`  

`<dl>`  
- `<dt>`
- `<dd>`  

`<ol>`  
- `<li>`
- `<ul>`

`<figure>`  
- `<img />`
- `<figcaption>`

`<div>` (block container)

### inline text semantics  

`<a>`  
- `href="https://example.com"`  
- `target="_self`(dafault)`/_blank/_parent/_top"`
- `rel="noopener/noreferrer"` (if target="_blank")  

`<q>`  
`<br />`  
`<b>`  
`<i>`  
`<em>`  
`<strong>`  

`<span>` (inline container)

### image and multimedia

`<img />`  
- `src="image.jpg"`  
- `alt`

### embedded content

`<picture>` (responsive)  
- `<source />`  
    - `srcset="image-one.jpg"`  
- `<img />`

### table content

`<table>`
- `<caption>`
- `<colgroup>`
    - `<col>`
        - `span`
- `<thead>` `<tbody>` `<tfoot>`
    -  `<tr>`
        -  `<th>`
            -  `scope="col/row"`
            -  `colspan/rowspan`
        -  `<td>`
            -  `colspan/rowspan`

### forms

`<form>`  
- `action`
- `method` (get/post)
- `target="_self`(dafault)`/_blank/_parent/_top"`  
don't use `action`, `method`, `target` - if handling form submission using javascript
- `enctype="application/x-www-form-urlencoded"` (default)

  `"multipart/form-data"` (if `<input type="file">`)

  `"text/plain"`
- `novalidate` (form validation)

`<label>`  
- `for` (id of `<input>`)

`<input />`  
- `type="checkbox/date/email/file/hidden/image/month/number/password/radio/search/tel/text/time/url/week"`
- `value` (for checkbox, radio, hidden)
- `id` 
- `name` 
- `placeholder` 
- `disabled` 
- `readonly` 
- `multiple`
- `required` (form validation)
- `min` (form validation)
- `max` (form validation)
- `minlength` (form validation)
- `maxlength` (form validation)
- `size` (form validation)
- `pattern` (form validation)

`<fieldset>`
- `<legend>`
- `<label>`
- `<input />`

`<select>`
- `<optgroup>`
    - `label`
    - `<option>`
        - `label`
        - `selected`

`<textarea>`
- `rows`
- `cols`

`<button>`
- `type="button/submit/reset"`

### interactive element

`<dialog>`
- `open`

### global attribute

`id`  
`class`   
`hidden`  
`title`  
`tabindex`  
`data-*` (to store your own custom data on elements and read it later in javascript using dataset property)  
`style` (inline css)  

### svg

`<svg>`

### icons

- icons in html
    - copy emoji/icons and paste
    - svg file in `<img>`
    - icon fonts (font awesome, material icons, etc)
    - inline `<svg>`
- icons in css
    - `background-image`
    - `::before/::after`
