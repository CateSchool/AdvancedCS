# 8. HTML & CSS

- [8. HTML & CSS](#8-html--css)
  - [Basic HTML Structure](#basic-html-structure)
    - [Tags](#tags)
      - [Text](#text)
      - [Lists](#lists)
      - [Links](#links)
      - [Media](#media)
      - [Forms](#forms)
      - [Section dividers](#section-dividers)
  - [CSS](#css)
    - [selectors](#selectors)
      - [ids](#ids)
      - [classes](#classes)

---

## Basic HTML Structure

**HTML (HyperText Markup Language)** is the basic building block of the Web. It is responsible for loading files and giving structure to web content. [Here's an HTML video overview](https://www.youtube.com/watch?v=PlxWf493en4).  
  
What goes in an HTML file?   
* The `<head></head>` is where we load files, libraries, and styles or set meta-data (e.g. site title).
* The `<body></body>` is where most of the elements thate will show up on the page should be placed (primarily what we're editing)
* Javascript files (scripts)
* CSS style sheets (more on this below)

There are two locations to load scripts. Rules from [SO](https://stackoverflow.com/questions/38407962/when-to-use-the-script-tag-in-the-head-and-body-section-of-a-html-page).

1. Place library scripts such as the p5.js library in the `<head>` section.
2. Place normal scripts in the `<head>` unless they become a performance/page load issue.
3. Place scripts that impact the render of the page (`sketch.js`) at the end of the `<body>`.


```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>website title</title>

    <!-- library scripts -->
    <script src="https://cdn.jsdelivr.net/npm/p5@1.3.1/lib/p5.js"></script>
  </head>
  <body>
    content of website ...

    <!-- scripts that affect webpage rendering -->
    <script src="script.js"></script>
  </body>
</html>
<html>
```


### Tags

#### Text

Headers:
```html
<h1>Header 1 Text</h1>
<h2>Header 2 Text</h2>
<h3>Header 3 Text</h3>
<h4>Header 4 Text</h4>
```

Paragraph:
```html
<p>Here is a paragraph of text...</p>
```

Bold:
```html
<strong>make it bold</strong>
```

Italics
```html
<em>make it bold</em>
```    

#### Lists
Ordered
```html
<ol>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
</ol>
```   

Unordered
```html
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
</ul>
```   

#### Links
```html
<a href="[PATH TO FILE / URL]">click me</a>
```   

#### Media
```html
<img src="[PATH TO IMAGE / URL]" />
```  

#### Forms
Buttons:

```html
<button onclick="myFunction()">click me!</button>
```

[Check out other HTML form elements here](https://www.w3schools.com/html/html_forms.asp).

#### Section dividers
  
Create a separate block (useful for customizing position / style of a block of HTML):

```html
<div style="color: red">
  <h1>Section</h1>
  <p>This is all a part of a section block that can be styled individually (more on this later)</p>
</div>
```

Select and style an **inline** element:

```html
<p>Here we will style <span style="color: blue">a portion of text</span>inside a paragraph etc.</p>
```

Create a horizontal line:  
`<hr />`

Create a line break:  
`<br />` 

## CSS

[Watch this video for an overivew](https://www.youtube.com/watch?v=1PnVor36_40).

CSS stands for Cascading Style Sheet and is used to add style to HTML elements. Where are going to look at 3 different ways to use CSS in an HTML file.


**1. Inline** - using the style attribute of an HTML element

```html
 <body style="background-color: lightblue">
```

**2. Internal** - how we can use `<style>` tags in the `<head>`to accomplish the same effect.

```html
<!-- other html -->
<head>
  <style>
    body {
      background-color: lightblue;
    }
    p {
      color:red;
    }
  </style>
</head>
<!-- other html -->
```

**3. External** - how we can use `<link>` tags in the `<head>`to load an external `style.css` file.

```html
<head>
  <!-- other code -->
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
```

### selectors

Notice in the examples below how we can specify all style of all tages, a combination of tags, or the children of tags:
 
```css
/* all divs */
div {

}

/* all divs AND all paragraphs */
div, p {

}

/* all paragraphs INSIDE (a.k.a. children) of divs */
div p {

}
```

#### ids
An **ID** is an attribute used to refer to (and style) a specific HTML element. Only one HTML element can have a particular ID. 


```html
<div id="About">
  <h1 id="pageTitle">About</h1>
  <p>Here is some information about me...</p>
</div>
```

In the `style.css`, we refer to an id with a "#":

```css
#About {
  border: 1px solid black;
}

#pageTitle {
  font-size: 200%;
}
```

We can specify child elements of an element identified with an ID:

```css
#About p {
  color: blue;
}
```


#### classes

A **class** is similar to an **ID** - it is a way to refer to specific HTML elements and give them style. The difference between an ID and a class is that unlike IDs where only one element can have a particular ID, *multiple elements* in the HTML can have the *same class*.

```html
<h1 class="big">First Paragraph</h1>
<p>Paragraph 1... here is some information.</p>
<h1 class="big">Second Paragraph</h1>
<p class="big">Paragraph 2... here is some information.</p>
```

In the `style.css`, we refer to classes with a "."

```css
.big {
    font-size: 200%;
}
```

If we wanted to refer specifically to h1 or p tags with the class "big":

```css
h1.big {
    font-size: 200%;
}
p.big {
  font-size: 120%;
}
```
