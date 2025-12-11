# QR code component solution

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

The production-ready website files are located in the `docs/` directory.

### Screenshot
<br>
![](qr-code-component-desktop-screenshot.jpg)

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
I wanted to ensure accessibility and inclusivity in my project. I learned that most screen readers cannot scan QR codes. To address this, I wrapped the QR code image in an anchor tag linking to Frontend Mentor's homepage and added an `alt` attribute that clearly describes the QR code's function.

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

However, I also learned that the `alt` attribute only works on the fallback `img` element, not the `source` element. For this reason, I decided to remove the fallback solution due to accessibility concerns.

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
During development, I noticed that my QR code component didn’t scale well on very small screens. Initially, I tried to fix this by reducing the HTML element’s font size to 50%, then using a media query to restore it to 100% on larger screens (min-width: 1440px). The idea was to effectively halve the component’s size on small and medium screens and return it to full size on larger ones.

However, adjusting the HTML element’s font size turned out to be the wrong approach. It caused my defined font sizes to fall below the browser’s minimum allowed font size. As a result, all text, regardless of my small, medium, or large font size definitions, rendered at the same minimum size.

I resolved the issue by restoring the HTML element’s font size to 100% and instead reduced the width, height, and font sizes of the QR code component itself. This makes the component appear smaller on mobile devices. I also added a new media query that doubles the component’s width, height, and font sizes on larger screens, ensuring it scales up appropriately.

While this was a quick and practical solution, I plan to continue refining a mobile-first approach and improving my skills in creating fully responsive applications.

### Useful resources

- [google-web-fonts-helper](https://gwfh.mranftl.com/fonts) - "A Hassle-Free Way to Self-Host Google Fonts"
- [Squoosh](https://squoosh.app/) - "Squoosh is an image compression web app that reduces image sizes through numerous formats."
- [Box-Shadow CSS Generator](https://html-css-js.com/css/generator/box-shadow/) - "Use the sliders and the color picker to set the values and watch the live preview until you reach the desired effect."
- [Markup Validator](https://validator.w3.org/) - "The Markup Validator is a free tool and service that validates markup: in other words, it checks the syntax of Web documents, written in formats such as (X)HTML."

## Author

- GitHub - [jbrown307](https://github.com/jbrown307)
- Frontend Mentor - [@jbrown307](https://www.frontendmentor.io/profile/jbrown307)
- LinkedIn - [Jordan Brown](https://www.linkedin.com/in/jordanbrownca/)

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


