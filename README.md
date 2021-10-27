# css

## CSS Specificity

> Specificity is a weight that is applied to a given CSS declaration, determined by the number of each selector type in the matching selector. When multiple declarations have equal specificity, the last declaration found in the CSS is applied to the element. Specificity only applies when the same element is targeted by multiple declarations. As per CSS rules, directly targeted elements will always take precedence over rules which an element inherits from its ancestor. - [MDN docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

The higher the specificity, the more difficult to override the rule.

#### Specificity Hierarchy

1. **Inline styles** - `<h1 style="color: #ffffff;">`
2. **IDs** - #id-name
3. **Classes, attributes and pseudo-classes** - .className, [attributes] and pseudo-classes such as :hover, :focus etc.
4. **Elements and pseudo-elements** - h1, div, :before and :after.
5. **Universal selector `(*)`** - applies to all elements (zero specificity)

## CSS Selectors

1. Universal selector `(*)` - it applies to all elements universally

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

all elements to include padding and borders in the box model calculation instead of adding those widths to any defined dimensions.

## Background Properties

```css
.hero-image {
  background-image: url("img.jpg"); /* The image used */
  /* background-image: linear-gradient(to right bottom, #7ed56f, #28b485), url(hero.jpg); */
  background-color: #cccccc; /* Used if the image is unavailable */
  height: 500px; /* You must set a specified height */
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
}
```

## clip-path

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
