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
