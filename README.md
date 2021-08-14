# Frontend Mentor - Meet landing page solution

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR). Frontend Mentor challenges help you improve your coding skills by building realistic projects!

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

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

Desktop view

![Solution preview](./assets/Screenshot_meet-landing-page.png)

### Links

- Solution URL: [Click here](https://www.frontendmentor.io/solutions/mobilefirst-meet-landing-page-6XaipbiNR)
- Live Site URL: [See live site here](https://juanbonilla.me/FEM_meet-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS / SASS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

I wanted to use `@mixin` in my solution to reduce the amount of lines of SCSS code. So, I decided to learn how to implement them by creating a `@mixin` to apply specific font properties. 

See below my solution for this:

```scss
@mixin title-font ($size, $line-height) {
    font-family: $f-family;
    font-size: $size;
    font-weight: 900;
    line-height: $line-height;
}

@mixin text-font ($size) {
    font-family: $f-family;
    font-size: $size;
    font-weight: 500;
    line-height: 1.625rem;
}
```
I wanted to have a block of code for titles and normal text. Then, I identified what values could be standar and which ones could change (those ones appear has parameters of the `@mixin`).

And below, it is explained how to call those `@mixin`:

```scss
.intro-title, .btn, .number p {
    @include title-font(1rem, 1.625rem);
}

.info {
    margin-bottom: 2rem;
    color: $gray;
    @include text-font(1rem);

    &--footer {
        color: $white;
        font-size: 1.125rem;
    }
}
```

### Continued development

I will continue improving my SCSS ability in order to create beatiful webpages with less code. I also want to reach pixel perfect based on the designs provided.

### Useful resources

- [@Mixin - SCSS](https://sass-lang.com/documentation/at-rules/mixin) - This helped me to create reusable blocks of SCSS code with the possibility to change specific values, because they can also take arguments.

## Author

- Website - [juanbonilla.me](https://juanbonilla.me)
- Frontend Mentor - [@juanpb96](https://www.frontendmentor.io/profile/juanpb96)
- LinkedIn - [Juan Bonilla](https://www.linkedin.com/in/juan-pablo-bonilla-6b8730115/)