---
title: "Functional programming with Javascript - "
subtitle: "Set up the project and environment"
author: [Stefan Sobek]
date: "2020-06-10"
subject: "An introduction course to functional programming with Javascript"
keywords: [Fontys, Markdown, Javascript, Function programming]
lang: "en"
titlepage: "true"
logo: "images/fontyslogo.png"
titlepage-rule-color: "400070"
page-background : "images/fontyslogo-background.png"
# reveal settings
# simple black white league beige sky night serif simple solarized blood moon
theme: black
separator: <!-- s -->
verticalSeparator: <!-- v -->
notesSeparator: <!-- n -->
revealOptions:
  # None - Fade - Slide - Convex - Concave - Zoom
  transition: 'concave'
  transition-speed: fast
  slideNumber: true
  history: true
  progress: true
  width: 1248
  height: 800
  parallaxBackgroundImage: 'images/fontys-parallax-all-dark.jpg'
  parallaxBackgroundSize: '2100px 1024px'
  #autoSlide: 4000
  #loop: true

  # center: false
...
---

# Functional Programming - Set up the project
<!-- .slide: data-background="images/slides-headline-background.jpg" -->

## Install Node.js and npm

### Node.js

- Node.js is a platform that allows to run JavaScript code outside the browser
- You do not need a webpage

- [Download Node.js](https://nodejs.org/en/)

![Node.js](images/0-nodejs-download.jpg)

- Install Node.js

### NPM

- NPM is the node package manager. Let us install it.
- Open a terminal/console/cmd line
- Type `npm install -g npm@latest`
- On Linux/Mac could be that you need to do `sudo npm install -g npm@latest`
- Check with `npm -v` if you can see the version of your npm package installation
- Check with `node -v` if you can see your node.js version


### Set up the project

- open Terminal/Shell/Cmd
- create a folder, e.g. inside Documents folder
- `cd Documents`
- `mkdir functional-js`
- `cd functional-js`
- `npm init -y`

![npm-init-2](images/0-setup-npm-2.gif)

<!-- s -->

### ES6 support with babel

- Currently node JS does not support ES6 Javascript code syntax. (e.g. chrome supports it natively)
- therefore we need to install an npm package

- Type `npm install --save @babel/core @babel/node @babel/preset-env`

![babel](images/0-setup-babel.gif)

### Editor

- You can use the editor of your choice with JS syntax support but we recommend:
  - [Visual Studio Code](https://code.visualstudio.com/)

### Hello World "normal JS"

- open the folder you created in your editor
- Create a file called `hello-world.js` and put th efollowing content:

```javascript
function hello(name) {
    console.log("Hello " + name);
}

hello("Luke Skywalker");
```

- now open the Terminal inside Visual Studio Code in the menu bar with: >Terminal >Open Terminal
- Then type: `node hello-world.js`

![hello world](images/0-hello-world.gif)

- This is with normal Javascript syntax

### Hello World "ES6 syntax - arrow functions"

