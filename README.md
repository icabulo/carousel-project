## Make It Real - Onboarding final challenge

# 09 Image Carousel

This is a solution to the Make It Real course final's project (onboarding sprint). It was done with SwiperJS.

## Table of contents

- [09 Image Carousel](#09-image-carousel)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
      - [**_HTML modifications_**](#html-modifications)
      - [**_Custom CSS_**](#custom-css)
      - [**_JS adjustments_**](#js-adjustments)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

### The challenge

In this project, we're going to create an image carousel.

what's nice with this project?

- I used [Swiper JS](https://swiperjs.com/demos).
- Centered image is used for user viewing focus.
- There are captions for the image's photo credits.
- Navigation:
  - Next and previous colored side buttons.
  - Clickable and Scrollable thumbnails.

### Screenshot

![My first image slider with Swiper JS](./images/readme/final.png)

## My process

### Built with

- [Swiper JS](https://swiperjs.com/demos).
- Flexbox & Grid.
- CSS custom properties.

### What I learned

I learned how to set up the Swiper library for slider demos using VS Code: JS, CSS, and HTML files.

First, I moved some HMTL tags for side buttons, then I created some container divs to make a custom layout for this project. Then I changed some CSS properties to personalize the slider style. Finally, I used API's documentation to tweak the JS file and adjust the default behavior, for example, fade out effect, number of thumbnails displayed, etc.

It was also nice that I had to use the browser's dev inspection tools vastly: to figure out the style properties and classes that dynamically change, for example, when the side buttons and thumbnails modify the elements displayed on the screen

#### **_HTML modifications_**

```html
<body>
  <!-- Swiper -->
  <div class="slider-component">
    <div class="slider-container">
      <div class="swiper-button-next"></div>
      <div class="swiper-button-prev"></div>
    </div>
  </div>
</body>
```

#### **_Custom CSS_**

```css
/* **************
custom properties 
***************** */

.slider-component {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
}
.slider-container {
  width: 70vw;
  height: 70vh;
}

.mySwiper .swiper-slide img:hover {
  border: 1px solid #ff00c7;
}
```

#### **_JS adjustments_**

```js
var swiper = new Swiper(".mySwiper", {
  spaceBetween: 10,
  slidesPerView: 5,
  freeMode: true,
  watchSlidesProgress: true,
});
```

### Continued development

The next step will be to include Swiper and React to get the same result.

### Useful resources

- [Swiper basics](https://youtu.be/bMy-mnqBtPk) - Nice tricks for adjusting buttons and css behavior..
- [Swiper set up](https://youtu.be/tOUlVIMqhcc) - Practical video to create a slider card and is also helpful for organizing JS and CSS separate files.

## Author

- github - [Ivan Cabulo](https://github.com/icabulo)

## Acknowledgments

Kudos to Sergio Jaramillo, our MIT mentor, for showing me the Swiper library.
