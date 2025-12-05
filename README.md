# Frontend Mentor - QR code component solution

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### Screenshot

![](./qr-code-component-screenshot.png)

### Links

- Solution URL: [Add solution URL here](https://github.com/jbrown307/qr-code-component/tree/main/src)
- Live Site URL: [Add live site URL here](https://jbrown307.github.io/qr-code-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Mobile-first workflow

### What I learned

**QR codes**
- Screen readers aren't able to scan QR codes. In order to solve this accessibility problem, I simply wrapped the QR code image in an achor tag that links to Frontend Mentor's home page.

- I was going to convert the QR code image into WebP in order to reduce its size while maintaining its visual quailty    

To see how you can add code snippets, see below:

```html
<picture>
  <a href="https://www.frontendmentor.io/" target="_blank">
  <source srcset="assets/image-qr-code.webp" type="image/webp">
  <img src="assets/image-qr-code.png" alt="QR code that links to frontend mentor's website.">
  </a>
</picture>
```
```css
.text p:nth-child(1) {
  font-weight: var(--font-weight-bold);
  font-size: var(--font-size-large);
  color: var(--slate-900)
    }

.text p:nth-child(2) {
  font-weight: var(--font-weight-regular);
  font-size: var(--font-size-medium);
  color: var(--slate-500);
    }
```

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [google-webfonts-helper](https://gwfh.mranftl.com/fonts) - This website allowed
me to self-host a Google font called "Outfit." This website hosts  
- [squoosh](https://squoosh.app/editor) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

## Author

- LinkedIn - [Jordan Brown](https://www.linkedin.com/in/jordanbrownca/)
- Frontend Mentor - [@jbrown307](https://www.frontendmentor.io/home)

