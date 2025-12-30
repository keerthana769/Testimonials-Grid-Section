
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
- [Acknowledgments](#acknowledgments)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

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

1. **Using border properties more clearly and explicitly**

  Instead of relying on shorthand, I learned how defining border styles and colors separately can improve clarity and control.
```css
border-style: solid;
border-color: A775F1;
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

  I practiced correctly setting up custom fonts with proper font weights and `font-display: swap` to improve user experience during loading.
```css
@font-face {
  font-display: swap; 
  font-family: 'Barlow Semi Condensed';
  font-style: normal;
  font-weight: 500;
  src: url('../fonts/barlow-semi-condensed-v16-latin-500.woff2') format('woff2'); 
}
```

4. **Positioning background images precisely**

  I learned how to control decorative background images using background-position to achieve better visual alignment across screen sizes.
```css
.feedback1 {
  background-image: url("./images/bg-pattern-quotation.svg");
  background-repeat: no-repeat;
  background-position: top right 10.5rem;
}
```

### Continued development

Going forward, I want to focus on improving my ability to match component sizes more accurately with the design. I plan to spend more time analyzing design files and experimenting with spacing, alignment, and sizing techniques to achieve a closer, more consistent visual result across all screen sizes.

### Useful resources

- [Resource 1](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes/rel/preload/) - This resource helped me understand how to preload fonts correctly to improve performance and avoid layout shifts during page load.
- [Resource 2](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/background-blend-mode/) - This article helped me better understand how background images and colors interact, and clarified when blending modes are useful in real layouts.


## Author

- Frontend Mentor - [@keerthana769](https://www.frontendmentor.io/profile/keerthana769)
- LinkedIn - [@keerthana-gurram](https://www.linkedin.com/in/keerthana-gurram/)



