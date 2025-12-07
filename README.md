# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

**Mobile Design**
![](,/qr-code-component-mobile-screenshot.jpg)

**Desktop Design**
![](./qr-code-component-desktop-screenshot.jpg)

### Links

- [Source Code](https://github.com/jbrown307/qr-code-component/tree/main/docs)
- [Live Site](https://jbrown307.github.io/qr-code-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

**Buliding Screen-Reader Friendy QR Codes**
<br>
I wanted to ensure accessibility and inclusivity in my project. I learned that most screen readers cannot scan QR codes. To address this, I wrapped the QR code image in an anchor tag linking to Frontend Mentor's homepage and added an alt attribute that clearly describes the QR code's function.

```html
<a href="https://www.frontendmentor.io/" target="_blank">
  <img src="assets/image-qr-code.png" alt="QR code that links to Frontend Mentor's website.">
</a>
```

**Combining Different Types of CSS Selectors**
<br>
I was able to reduce the number of classes in the HTML by combining multiple types of selectors. For example, to style two paragraph elements, I used a compound selector combining class, descendant, and pseudo selectors:

```css
.text-container p:nth-child(1) {
  font-weight: var(--font-weight-bold);
  font-size: var(--font-size-large);
  color: var(--slate-900);
}

.text-container p:nth-child(2) {
  font-weight: var(--font-weight-regular);
  font-size: var(--font-size-medium);
  color: var(--slate-500);
}
```

**Exploring Different Image Formats**
<br>
Initially, I considered reducing the file size of the QR code image to improve performance. However, I realized it’s best to maintain high image quality for QR codes to ensure reliable scanning.

I explored converting the QR code to modern formats like WebP or AVIF, which offer a good balance of file size and quality. However, older browsers may not support these formats, so I implemented a solution using WebP for modern browsers and PNG as a fallback.

I also learned that the alt attribute only works on the fallback <img> element, not the <source> element.

```html
<picture>
  <a href="https://www.frontendmentor.io/" target="_blank">
    <!-- Use WebP if the browser supports it -->
    <source srcset="assets/image-qr-code.webp" type="image/webp">
    <!-- fallback to PNG image for older browsers -->
    <img src="assets/image-qr-code.png" alt="QR code that links to Frontend Mentor's website.">
  </a>
</picture>
```

### Continued development
During development, I noticed that my QR code component didn’t scale well on very small screens. I solved this by reducing the HTML element's font size to 50% and using a media query to restore it to 100% on larger screens (min-width: 1440px).

This approach effectively halved the component size on small and medium screens and restored it on larger screens. While this was a quick and practical solution, I plan to continue refining a mobile-first approach and improving my skills in creating fully responsive applications.

### Useful resources

- [google-web-fonts-helper](https://gwfh.mranftl.com/fonts) - "A Hassle-Free Way to Self-Host Google Fonts"
- [Squoosh](https://squoosh.app/) - "Squoosh is an image compression web app that reduces image sizes through numerous formats."

## Author

- GitHub - [jbrown307](https://github.com/jbrown307)
- Frontend Mentor - [@jbrown307](https://www.frontendmentor.io/profile/jbrown307)
- LinkedIn - [Jordan Brown](https://www.linkedin.com/in/jordanbrownca/)

