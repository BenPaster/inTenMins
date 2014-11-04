# Learn CSS In 10 Minutes
Because it's really not that hard. This does assume some minimal, confused knowledge.

### Including a separate CSS file
Including `<style></style>` tags in the HTML file's `<head>` section usually isn't the answer.

```html
<link rel="stylesheet" href="myCSSFile.css" media="screen" charset="utf-8">
```

### The format of every single CSS block
Seriously, they all work this way. OK fine there are some exceptions but they're for complicated stuff.
```css
/* This is the only way to make a comment in CSS */
selector:psuedo-class {
  property: value;
  anotherProp: anotherVal;
}
```

### Selectors
```
p
div
#theIdOfYourHTMLElement
.theClassOfYourHTMLElement
```

### Psuedo Classes
That you'll use anytime soon.
```
:hover
:link
:visited
:first-child
:last-child
```

### Properties 
This is how you actually add style to the stuff on your website. [This list](http://www.w3schools.com/cssref/) is from w3schools which has some pretty mediocre stuff a lot of the time, but this list looks pretty good for getting an idea of what properties you can use.

### When to use an element name
```html
<p>Paragraph 1</p>
<p>Paragraph 2</p>
```

```css
p {
  color: red;
}
```
Paragraph 1 and Paragraph 2 will be colored red

### When to use a dot (class selector)
```html
<div class="smile"></div>
```
```css
.smile {
  property: value;
}
```

### When to use a hash (id selector)
```html
<div id="smile"></div>
```
```css
#smile {
  property: value;
}
```

### Multiple classes?
```html
<div class="smile blue"></div>
<div class="smile red"></div>
```
This is really useful because you can define a "base class" and then make modifications based on more specific element types.
```css
.smile {
  /* 
    The following could be written as padding: 5px 10px; 
    Why? padding (and margin) is special and it can work like
    padding: top right bottom left;
  */
  padding-left: 10px;
  padding-right: 10px;
  padding-top: 5px;
  padding-bottom: 5px;
}

/* This is very specific and only works on smile elements. Maybe you just want .blue to turn any type of element blue. */
.smile.blue { 
  background-color: #36abdb;
}

.smile.red { 
  background-color: #df4e4e;
}
```

### Mix and Match selectors
```css
/* All paragraphs with the class .blue will be colored blue */
p.blue {
  color: blue;
}

/* All paragraphs with the id #blue will be colored blue */
p#blue {
  color: blue;
}

/* You can do the same thing with Ids and classes  */
#text.blue {
  color: blue;
}
```
