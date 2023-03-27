# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Links

- Solution URL: https://github.com/anwari-fikri/testimonials-grid-section
- Live Site URL: https://anwari-fikri.github.io/testimonials-grid-section/

## My process

### Built with

- Flexbox
- Grid
- Mobile-first workflow
- Tailwind

### What I learned

### 1. Grid lines start at 1, not 0

I tried something like:

```
<div class="grid grid-rows-3 grid-flow-col gap-4">
  <div class="row-span-1 ...">01</div>
  <div class="col-span-1 ...">02</div>
  <div class="row-span-0 ...">03</div>
</div>
```

Which does not work because grid lines starts from 1 not 0.

So, we have to change the code to this:

```
<div class="grid grid-rows-3 grid-flow-col gap-4">
  <div class="row-span-1 ...">01</div>
  <div class="col-span-1 ...">02</div>
  <div class="row-span-0 ...">03</div>
</div>
```

### 2. Using z-index for bg-pattern-quotation.svg

If I want to use negative z-index, i first must have z-index for positive first.

For example, having a -z-10 as it is will not work:

```
<div
  class="relative ..."
>
  <img
    src="./images/bg-pattern-quotation.svg"
    class="absolute -z-10 top-0 right-0 mr-24"
  />
  <p>
    I received a job offer mid-course, and the subjects I learned were
    current, if not more so, in the company I joined. I honestly feel I
    got every penny’s worth.
  </p>
</div>
```

To fix this, we need a positive z-index (example, z-10) either in the div or the p tag depending on whats needed:

```
<div
  class="relative z-10 ..."
>
  <img
    src="./images/bg-pattern-quotation.svg"
    class="absolute -z-10 top-0 right-0 mr-24"
  />
  <p>
    I received a job offer mid-course, and the subjects I learned were
    current, if not more so, in the company I joined. I honestly feel I
    got every penny’s worth.
  </p>
</div>
```

## Author

- Website - [Anwari Fikri](https://www.anwarifikri.com/)
- Frontend Mentor - [@anwari-fikri](https://www.frontendmentor.io/profile/anwari-fikri)
