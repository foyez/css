# CSS (Cascading Style Sheets)

- Used to describe the presentation of a document written in **HTML**

CSS Example 🧮

```css
selectorA {
  property1: value1;
}

body {
  color: white;
}
```

## Including CSS

<details>
<summary>View contents</summary>

External Style Sheet

```html
<link href="stylesheet" href="file.css" />
```

Embedded Styles

```html
<style>
  body {
    background-color: gray;
  }
</style>
```

Inline Styles

```html
<p style="color:black">Lorem ipsum</p>
```

</details>

## CSS Box Model

<details>
<summary>View contents</summary>

> The CSS box model refers to how HTML elements are modeled in browser engines and how the dimensions of those HTML elements are derived from CSS properties.

<img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/Boxmodell-detail.png" alt="the box model" />
  
```css
/********************** CONTENT *************************
The box that contains the actual element content like text, 
image, icon, gif, video,... */

tag_name {
height: 90px;
width: 200px;
}

/\***\*\*\*\*\***\*\*\***\*\*\*\*\*** PADDING \***\*\*\*\*\*\*\***\*\***\*\*\*\*\*\*\***
Distance between the content and the border. The background color,
of the element will never affect this space. But you can see this by
contrasting with the background color of the parent element that
contains your element\*/

tag_name {
padding-top: 50px;
padding-right: 30px;
padding-bottom: 50px;
padding-left: 80px;
}

/_OR: _/

tag*name {
padding: 25px 50px 75px 100px; /* top; right; bottom; left \_/
}

tag*name {
padding: 25px 50px 75px; /\* top; right*&\_left; bottom \*/
}

tag*name {
padding: 25px 50px; /\* top*&_bottom; right_&\_left \*/
}

tag*name {
padding: 25px; /\* top*&_bottom_&_right_&\_left \*/
}

/\***\*\*\*\*\***\*\*\***\*\*\*\*\*** BORDER \***\*\*\*\*\*\*\***\*\***\*\*\*\*\*\*\***
You can define a frame for your element's box. You can
only see the border, after you define a style for that
property \*/

tag*name {
border-width: 5px 70px 10px 28px; /* or border-bottom-width: 10px; ... _/
border-color: blue; /_ or border-top-color: #b52e2e; ... _/
border-style: dotted; /_ or dashed, or solid, or ... _/
border-radius: 70% /_ making the corners more rounded \_/
}

/_OR: _/

tag*name {
border: 5px solid red; /* all*widths; style; color */
}

tag*name {
border-left: 6px dotted green; /* width; style; color _/
border-top: 34px groove yellow; /_ width; style; color \_/
}

/\***\*\*\*\*\***\*\*\***\*\*\*\*\*** OUTLINE \***\*\*\*\*\*\*\***\*\***\*\*\*\*\*\*\***
It's a line that's drawn around your html element, but
contrary to the border, the dimensions of the outline
aren't taken into account. It's drawn around elements,
outside the borders, to make the element "stand out" \*/

tag*name {
outline-width: thin; /* or medium; thick; outline-width: 4px; ... _/
outline-color: blue; /_ or #b52e2e; invert; ... _/
outline-style: dotted; /_ or dashed, or solid, or ... _/
outline-offset: /_ making the corners more rounded \_/
}

/_OR: _/

tag_name {
outline: dashed;  
}

tag_name {
outline: dotted red;
}

tag*name {
outline: 5px solid yellow; /* all*widths; style; color */
}

tag_name {
outline: thick ridge pink;
}

/\***\*\*\*\*\***\*\*\***\*\*\*\*\*** MARGIN \***\*\*\*\*\*\*\***\*\***\*\*\*\*\*\*\***
This is the distance that separates an html element,
from the other elements around it. The background color,
of the element will never afect this space, because the
margin doesn't have background color. The margin is an
invisible border or space between two objects \*/

tag_name {
margin-top: 100px;
margin-bottom: 100px;
margin-right: 150px;
margin-left: 80px;
}

/_OR: _/

tag*name {
margin: 25px 50px 75px 100px; /* top; right; bottom; left \_/
}

tag*name {
margin: 25px 50px 75px; /\* top; right*&\_left; bottom \*/
}

tag*name {
margin: 25px 50px; /\* top*&_bottom; right_&\_left \*/
}

tag*name {
margin: 25px; /\* top*&_bottom_&_right_&\_left \*/
}

````

</details>

## CSS Specificity

<details>
<summary>View contents</summary>

> Specificity is a weight that is applied to a given CSS declaration, determined by the number of each selector type in the matching selector. When multiple declarations have equal specificity, the last declaration found in the CSS is applied to the element. Specificity only applies when the same element is targeted by multiple declarations. As per CSS rules, directly targeted elements will always take precedence over rules which an element inherits from its ancestor. - [MDN docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

The higher the specificity, the more difficult to override the rule.

#### Specificity Hierarchy

1. **Inline styles** - `<h1 style="color: #ffffff;">`
2. **IDs** - #id-name
3. **Classes, attributes and pseudo-classes** - .className, [attributes] and pseudo-classes such as :hover, :focus etc.
4. **Elements and pseudo-elements** - h1, div, :before and :after.
5. **Universal selector `(*)`** - applies to all elements (zero specificity)

</details>

## CSS Selectors

<details>
<summary>View contents</summary>

1. Universal selector `(*)` - it applies to all elements universally

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
````

all elements to include padding and borders in the box model calculation instead of adding those widths to any defined dimensions.

</details>

## Background Properties

<details>
<summary>View contents</summary>

```css
.hero-image {
  background-image: url('img.jpg'); /* The image used */
  /* background-image: linear-gradient(to right bottom, #7ed56f, #28b485), url(hero.jpg); */
  background-color: #cccccc; /* Used if the image is unavailable */
  height: 500px; /* You must set a specified height */
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
}
```

</details>

## clip-path

<details>
<summary>View contents</summary>

The clip-path property in CSS allows you to specify a specific region of an element to display, with the rest being hidden (or “clipped”) away.

```css
.clip-me {
  /* Example: clip away the element from the top, right, bottom, and left edges */
  clip-path: inset(10px 20px 30px 40px); /* or "none" */

  /* Example: clip element into a Triangle */
  clip-path: polygon(50% 0%, 100% 100%, 0 100%);
}
```

[CSS clip-path maker](https://bennettfeely.com/clippy/)

</details>

## CSS Tips & Tricks

<details>
<summary>View contents</summary>

#### 1. [Centering in CSS: A Complete Guide](https://css-tricks.com/centering-css-complete-guide/)

</details>
