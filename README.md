
## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](./images/Screenshot.png)

### Links

- Solution URL: [GitHub Repository](https://github.com/keerthana769/Testimonials-Grid-Section/)
- Live Site URL: [Live Demo](https://keerthana769.github.io/Testimonials-Grid-Section/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

1. **Understanding border properties (shorthand vs individual values)**

  I learned how to use CSS borders both with shorthand and individual properties, and when to choose clarity over conciseness when styling borders.
```css
.img{
  border-style: solid;
  border-color: #A775F1;
  border-width: 2px;
}
  /* Shorthand version */
.img{
  border: 1px solid #A775F1;
}
```

2. **Preloading fonts to improve performance**

  I learned how to preload custom fonts to ensure they load faster and reduce layout shifts during page rendering.
```html
<link
  rel="preload"
  href="fonts/barlow-semi-condensed-v16-latin-500.woff2"
  as="font"
  type="font/woff2"
  crossorigin />
```

3. **Defining custom fonts using @font-face**

  - I practiced correctly setting up custom fonts with proper font weights and `font-display: swap` to improve user experience during loading.
```css
@font-face {
  font-display: swap; 
  font-family: 'Barlow Semi Condensed';
  font-style: normal;
  font-weight: 500;
  src: url('../fonts/barlow-semi-condensed-v16-latin-500.woff2') format('woff2'); 
}
```
  - `font-display: swap` Shows the text immediately using a fallback font. When the custom font is ready, swap it in.

4. **Positioning decorative background images responsively**

  I learned how to control decorative background images using `background-position` to achieve better visual alignment across screen sizes. Instead of copying fixed pixel values directly from Figma, converting positions to percentages helps achieve a more responsive and scalable result.

```css
.feedback1 {
  background-image: url("./images/bg-pattern-quotation.svg");
  background-repeat: no-repeat;
  background-position: 70% 0%;
}
```
  **Converting Figma values to responsive CSS**

  If Figma shows:
  * X position: `376px`
  * Container width: `540px`

  Formula:
  (image X / container width) × 100
  Result:
  (376 / 540) × 100 ≈ 69.6%

5. **Understanding opacity values in CSS colors**

  I learned that the rgb() function does not support opacity values. When opacity is required, rgba() must be used instead. CSS opacity values range from 0 to 1, not percentages, so values from design tools like Figma need to be converted. Figma opacity 24.74% converts to 0.2474

```css
box-shadow: 40px 60px 50px -47px rgba(72, 85, 106, 0.2474);
```

6. **Correctly using curly quotes in HTML**

  - Curly (typographic) quotes should be included using HTML entities, not typed directly into attributes.
  - This avoids encoding issues and ensures consistent rendering across browsers.
  - Curly quotes should be used only in text content, never in HTML attributes.
  - Common HTML entities for curly quotes:
      Left double	&ldquo;	“
      Right double	&rdquo;	”
      Left single	&lsquo;	‘
      Right single	&rsquo;	’
  - Example usage in HTML:
```html
<p>&ldquo;Learning HTML the right way matters.&rdquo;</p>
```
7. **Understanding margin collapsing and logical properties**

  - I learned that vertical margins collapse, while horizontal margins do not, which explains why margin-inline and margin-block behave differently when applied to the body.
  - margin-inline adds space to the left and right of the body, reducing the available width for its children. As a result, cards shift inward even though no margin is applied directly to them.
  - margin-block adds space to the top and bottom, but these vertical margins collapse between the body and its first or last child, causing the entire layout to move as a single block rather than squeezing individual cards.

  - Best practice: Avoid using margins on the body for layout. This approach prevents margin-collapsing issues and keeps layout behavior predictable.
```css
body {
  margin: 0;
}

.container {
  max-width: 1110px;
  margin: 83px auto;
  padding-inline: 60px;
}
```

8. **Letting grid items size themselves based on content**

- Using 1fr forces grid tracks to fill available space, not fit content.
- Rows are auto by default and naturally size themselves based on their content.
- Recommended approach for content-based rows: `grid-auto-rows: auto;`
- This tells the grid: Rows should be as tall as their content.


### Continued development

Going forward, I want to improve how accurately I translate designs into code by focusing more on component sizing, spacing, and alignment to achieve consistent results across screen sizes. I also want to deepen my understanding of horizontal and vertical margins, as well as how decorative background images are positioned and handled in CSS.

### Useful resources

- [Resource 1](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes/rel/preload/) - This resource helped me understand how to preload fonts correctly to improve performance and avoid layout shifts during page load.
- [Resource 2](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/background-blend-mode/) - This article helped me better understand how background images and colors interact, and clarified when blending modes are useful in real layouts.


## Author

- Frontend Mentor - [@keerthana769](https://www.frontendmentor.io/profile/keerthana769)
- LinkedIn - [@keerthana-gurram](https://www.linkedin.com/in/keerthana-gurram/)
