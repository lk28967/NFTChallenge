# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Links

- Solution URL: [Add solution URL here](https://github.com/lk28967/NFTChallenge.git)
- Live Site URL: [Add live site URL here](https://lk28967.github.io/NFTChallenge/)

## My process

I started out planning to use Bootstrap, as I've been using it a lot for the current site I'm working on and I feel like it simplifies so much, and I was hoping to get some more practice with it. The issue I ran into is that my site already had Bootstrap connected when I started working on it, so I was clueless as to how to actually get it working in the first place. I decided to skip it and go the more manual route. I used quite a bit of flexbox to get everything in position, and after that added the styling. Those two parts were pretty easy and didn't take much thought. THEN I had to add the hover states and that's when everything went wrong. Specifically, the image hover state was my biggest challenge. I've never had to make a new image pop up on hover, so that alone was confusing, but then I also had to get the background color to change alongside it's opacity. I just kept trying things and Googling a lot, and eventually it was working! I honestly can't even say how, it was by some miracle and I stopped messing with it for fear of breaking it! After that, since I'd made everything responsive out of habit, I had to go through and change all rems/vw's to pixels. I added a box shadow and then I was done!

### Built with

Flexbox

### What I learned

The number one thing I learned doing this was how to add images as hover states for other images. After some effort, this was my HTML: 

  <div class="images">
    <img class="image-main" src="images/image-equilibrium.jpg">
    <img class="image-hover" src="images/icon-view.svg">
  </div>

  And my CSS:

.images {
    background-color:hsl(178, 100%, 50%);
    border-radius: 8px;
    max-width: 294px;
    max-height: 294px;
    position: relative;
    display: inline-block;
}

.image-main {
    width: 295px;
    max-height: 295px;
    border-radius: 6px;
    position: relative;
    display: inline-block;
}

.images .image-hover {
    display: none;
    position: absolute;
    padding: 125px;
    border-radius: 6px;
    top: 0;
    left: 0;
    z-index: 99;
}

.images:hover .image-main {
    z-index: 99;
    opacity: 50%;
}

.images:hover .image-hover {
    display: inline;
    cursor: pointer;
}

I'm sure this was far more complicated than it needed to be, and I'm sure I'll eventually figure out a simpler way to do it, but for now, this worked and I was happy!

### Continued development

While I learned how to do the image hover, I definitely would not say I'm comfortable with it. I'd like to keep practicing that. Also, flexbox! Possibly my favorite layout tool, and definitely something I want to continue using in future projects.

### Useful resources

- https://www.tutorialrepublic.com/faq/how-to-change-image-on-hover-with-css.php This resource was the one that finally helped me with the image hover. I tried many different solutions before this one that all failed! It took some adapting to get to work for this specific project, but it gave me the base code.

## Author

- Website - (https://laurakaneart.com/)
- Frontend Mentor - [@lk28967](https://www.frontendmentor.io/profile/yourusername)