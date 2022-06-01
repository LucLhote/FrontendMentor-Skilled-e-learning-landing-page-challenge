# Frontend Mentor - Skilled e-learning landing page solution

This is a solution to the [Skilled e-learning landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/skilled-elearning-landing-page-S1ObDrZ8q). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
    - [Problems encountered with the overflow property in CSS](#problems-encountered-with-the-overflow-property-in-css)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./design/presentation-result.png)

### Links

- Solution URL: [https://github.com/LucLhote/FrontendMentor-Skilled-e-learning-landing-page-challenge](https://github.com/LucLhote/FrontendMentor-Skilled-e-learning-landing-page-challenge)
- Live Site URL: [https://luclhote.github.io/FrontendMentor-Skilled-e-learning-landing-page-challenge/](https://luclhote.github.io/FrontendMentor-Skilled-e-learning-landing-page-challenge/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

#### Problems encountered with the overflow property in CSS

What was interesting to work on was the image for the tablet and desktop windows. I was a bit confused because I was using the ``overflow-x`` property and the ``hidden`` value but it was like using the ``overflow`` property for both axes. I realized that it gave the same value for the default ``overflow-y`` property. I tried adding the ``overflow-y`` property with the value ``visible`` but nothing changed. My image was with hidden overflow for both axes. 

I changed my approach and decided to use absolute and relative position, and came to a good result. I've never had to position an image in this setup and tried to find the easiest and cleanest way to do it for the next time I need to.

Code example:
```css
/* Class for the parent block of my image */
.head-section__col2 {
    width: 100%;
    height: auto;
    position: absolute;
    z-index: -1; /* It allows the block not to be above the buttons of the header and the first section */
    top: 0;
    left: 0;
    overflow: hidden;
}

.head-section__hero-image-tablet {
    width: auto;
    height: 45rem;
    display: block;
    position: relative;
    top: -5.3125rem;
    right: -18.4375rem;
}
```

Going back to the ``overflow`` property, just my way of doing it was not right. I found a way to use ``overflow-x`` and ``overflow-y`` on a blog called Katastross to get the result I was looking for ([Article: The problem when one of overflow-x/y is set to visible but the other is not](https://blog.katastros.com/a?ID=01600-5d66771b-0f48-4f9f-8da6-09880726ab97)).

### Continued development

I'd like to see how to do with button hover on mobile and tablet views.

### Useful resources

- [The problem when one of overflow-x/y is set to visible but the other is not](https://blog.katastros.com/a?ID=01600-5d66771b-0f48-4f9f-8da6-09880726ab97) - This helped me to understand why my way to use ``overflow-x`` and ``overflow-y`` wasn't good.
- [CSS overflow-x: visible; and overflow-y: hidden; causing scrollbar issue](https://stackoverflow.com/questions/6421966/css-overflow-x-visible-and-overflow-y-hidden-causing-scrollbar-issue) - Helped me confirm the problem.

## Author

- Email - [luc.lhote@outlook.com](luc.lhote@outlook.com)
- Frontend Mentor - [@LucLhote](https://www.frontendmentor.io/profile/LucLhote)
- LinkedIn - [Luc Lhote](https://www.linkedin.com/in/luclhote/)
- freeCodeCamp - [@LucLh](https://www.freecodecamp.org/LucLh)
- freeCodeCamp Forum - [@LucLh](https://forum.freecodecamp.org/u/luclh/summary)