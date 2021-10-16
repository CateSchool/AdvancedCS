# 8. HTML & CSS

- [Basic Structure](#basic-structure)
- [Tags](#tags)
  - [text](#text)
  - 

---

## Basic Structure

For the most part, you will be editing the contents inside `<body></body>`. This is where most of the elements thate will show up on the page should be placed.

The `<head></head>` is where 

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


## Tags
### text
* headers, 
* paragraph
* strong
* em
    
#### Lists
* ordered
* unordered

#### Links
* links

#### media
* images
* videos

#### Forms
* buttons
* forms

#### Section dividers
* section dividers
  * divs, span
  * <hr />
  * <br />

## Scripts
Rules from [SO](https://stackoverflow.com/questions/38407962/when-to-use-the-script-tag-in-the-head-and-body-section-of-a-html-page).

1. Place library scripts such as the p5.js library in the head section.
2. Place normal scripts in the head unless they become a performance/page load issue.
3. Place scripts that impact the render of the page (`sketch.js`) at the end of the body.