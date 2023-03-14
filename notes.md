# FrontEndMasters Bootcamp Notes

## HTML Resources

<https://frontendmasters.github.io/bootcamp/html>

HTML Elements Reference

<https://developer.mozilla.org/en-US/docs/Web/HTML/Element>

InternetingIsHard.com

    Introduction https://internetingishard.com/html-and-css/introduction/

    Basic Web Pages https://internetingishard.com/html-and-css/basic-web-pages/

    Links and Images https://internetingishard.com/html-and-css/links-and-images/

    Semantic HTML https://internetingishard.com/html-and-css/semantic-html/

Validating HTML

<http://validator.w3.org/>

## CSS

### Terminology

    p { font-weight: bold;
        font-family: Arial, sans-serif; }

font-weight is a property  
bold        is a value  
{ font-weight: bold; font-family: Arial, sans-serif; }  is a declaration block (made of individual declarations)  
p           is a selector  

### How to include CSS in HTML

External stylesheet : attach a separate document in the head of your HTML.

    <link href="css/styles.css" rel="stylesheet" />

Internal stylesheet or embedded stylesheet : Include styles in the style tag in the head of your HTML

    <style>
        body {
            font-family: Arial, Helvetica, sans-serif;
        }
    </style>

Inline styles : occur in the HTML tag itself

    <p style="color: purple;">I am a purple paragraph!</p>

### CSS Selectors

Four simple ways to include CSS in your document:

- Elements: HTML tags as selectors
- Classes
- IDs
- Descendant selector

#### Element Selectors

Simply list the HTML tag and how you'd like it styled.

    body {
        font-family: Arial, Helvetica, sans-serif;
    }

#### Class Selectors

Create a class and attach it to an HTML tag to make the class appear.

    .classname

    <style>
    .warning {
        color: orange;
        font-weight: bold;
    }
    </style>

    <p class="warning">This paragraph displays a warning!</p>

- An element can be of more than one class.
- You may use classes in different parts of the document.
- Classes are more specific than HTML elements and override them.

#### ID Selectors

Create an ID and attach it to an HTML tag to make the styling appear.

    <style>
        #danger {
            color: red;
            font-weight: bold;
            text-transform: uppercase;
        }
    </style>

    <p id="danger">This text is uppercase, bold, and red, and you better pay attention because you're in danger only once on this web page!</p>

#### Descendant selectors .classname element {}

This is a combination of one or more classes, IDs, or elements, separated by spaces, to indicate a family relationship.

    <style>
    .warning p {
        color: violet;
    }
    </style>

    <article class="warning">
        <p>All paragraphs in this article will have a color of violet.</p>
        <p>This paragraph too! No more classes needed!</p>
    </article>

### Link Pseudo-classes

Pseudo-classes: specify styling in these states.

    :link — unvisited link
    :visited — visited state
    :focus — the currently "focused" (selected) element
    :hover — hover your mouse over this
    :active — the time between the link is selected and the time the page loads. (Not used much today.)

If you are using these pseudo-classes, they MUST go in the order listed.

To remember: **Lord Vader Former Handle Anakin**

Use the `::before` selector to insert something before the content, or `::after` to do it after the content.

### CSS Variables

    Info taken from: https://www.w3schools.com/css/css3_variables.asp

The `var()` function is used to insert the value of a CSS variable.

The syntax of the `var()` function is as follows:

    var(--name, value)

    Value  Description
    name  Required. The variable name. Must start with two dashes and is case sensitive.
    value  Optional. The fallback value. Used if the variable is not found.

CSS variables can have a global or local scope.

Global variables can be accessed/used through the entire document, while local variables can be used only inside the selector where it is declared.

To create a variable with global scope, declare it inside the `:root` selector. The `:root` selector matches the document's root element.

To create a variable with local scope, declare it inside the selector that is going to use it.

See `--high-color` example in `styles.css`.

### Box Model

See box-model.html and box-model.css for basic examples.
See <https://frontendmasters.github.io/bootcamp/layout> for a wide range of very clear examples.

*To blog about*:

- Box Model
- Floats and Clears
    <https://codepen.io/vaniaschmied/pen/YzOrWKB>

- Styling Navigation Bars
- Flexbox

### Further learning

From <https://frontendmasters.github.io/bootcamp/layout>

    Box Model Types (Content vs. Border)

Forms...

CSS Media Queries: <https://www.w3schools.com/css/css3_mediaqueries.asp>
And many other topics in **w3schools**.

### CSS References

InternetingIsHard.com

- Hello CSS <https://internetingishard.com/html-and-css/hello-css/>
- CSS Selectors <https://internetingishard.com/html-and-css/css-selectors/>
- Links and Images <https://internetingishard.com/html-and-css/links-and-images/>

**Validating CSS**: <http://jigsaw.w3.org/css-validator/>

**Convert pixels to ems and %**: <http://www.pxtoem.com/>

**Color palettes**, if you need help creating one: <http://color.adobe.com/>

**Colorzilla**, for choosing colors from your website: <http://www.colorzilla.com/>
