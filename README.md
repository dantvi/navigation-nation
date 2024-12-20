# Navigation Nation

This project demonstrates an animated and responsive navigation menu created as part of the course "JavaScript Web Projects: 20 Projects to Build Your Portfolio" by Zero To Mastery. The navigation features smooth animations and an interactive menu overlay, providing a modern and engaging user experience.

## Table of contents

- [Navigation Nation](#navigation-nation)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

This project includes the following features:
- A mobile-first, responsive navigation menu.
- A toggleable overlay menu with smooth animations for opening and closing.
- Navigation links that animate dynamically with delays for a polished appearance.
- Customizable color schemes and animations.

### Screenshot

![](./screenshot.png)

### Links

- Live Site URL: [DT Code](https://navigation-nation.dtcode.se/)

## My process

### Built with

- HTML5 for semantic structure.
- CSS3 for styling and animations. 
  - Custom properties (CSS variables).
  - Keyframe animations.
- JavaScript (ES6+) for interactivity.
  - DOM manipulation.
  - Event listeners.
  - Dynamic class toggling.

### What I learned

In this project, I gained experience with:
- Creating animated navigation menus using CSS keyframes and JavaScript.
- Implementing dynamic animations for both the navigation links and the menu overlay.
- Using the classList.replace() method to dynamically switch classes and control animations.
- Building responsive layouts with mobile-first design principles.

For example, here’s the code for controlling navigation animations:

```js
function navAnimation(direction1, direction2) {
    navItems.forEach((nav, i) => {
        nav.classList.replace(`slide-${direction1}-${i + 1}`, `slide-${direction2}-${i + 1}`);
    });
}

function toggleNav() {
    menuBars.classList.toggle('change');
    overlay.classList.toggle('overlay-active');
    if (overlay.classList.contains('overlay-active')) {
        overlay.classList.replace('overlay-slide-left', 'overlay-slide-right');
        navAnimation('out', 'in');
    } else {
        overlay.classList.replace('overlay-slide-right', 'overlay-slide-left');
        navAnimation('in', 'out');
    }
}
```

### Useful resources

- [MDN Web Docs: CSS Keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes) - Used for creating smooth animations.
- [CSS Variables Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) - Helped in organizing color schemes.
- [Unsplash](https://unsplash.com/) - Provided the background image for the homepage.

## Author

- GitHub - [@dantvi](https://github.com/dantvi)
- LinkedIn - [@danieltving](https://www.linkedin.com/in/danieltving/)

## Acknowledgments

Special thanks to Zero To Mastery for providing the course and inspiration for this project. Thanks also to MDN Web Docs for excellent documentation on CSS and JavaScript.
