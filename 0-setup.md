---
title: "Functional programming with Javascript - "
subtitle: "Set up the project and environment"
author: [Stefan Sobek]
date: "2021-01-01"
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

# Functional Programming with Javascript

## Set up the project

<!-- s -->

## Install Node.js

- Node.js is a platform that allows to run JavaScript code outside the browser<!-- .element: class="fragment fade-up" -->
- You do not need a webpage<!-- .element: class="fragment fade-up" -->

[Download Node.js](https://nodejs.org/en/)<!-- .element: class="fragment fade-up" -->

<!-- s -->

![Node.js](images/0-nodejs-download.jpg)

<!-- s -->

## Install NPM

- NPM is the node package manager. Let us install it.<!-- .element: class="fragment fade-up" -->
- Open a terminal/console/cmd line<!-- .element: class="fragment fade-up" -->
- Type:<!-- .element: class="fragment fade-up" -->

`npm install -g npm@latest`<!-- .element: class="fragment fade-up" -->

- On Linux/Mac could be that you need to do: <!-- .element: class="fragment fade-up" -->

`sudo npm install -g npm@latest`<!-- .element: class="fragment fade-up" -->

- Check your versions with:<!-- .element: class="fragment fade-up" -->

`npm -v` <!-- .element: class="fragment fade-up" -->

`node -v` <!-- .element: class="fragment fade-up" -->

<!-- s -->

### Set up the project

- open Terminal/Shell/Cmd<!-- .element: class="fragment fade-up" -->
- create a folder, e.g. inside Documents folder<!-- .element: class="fragment fade-up" -->

```bash
cd Documents
mkdir functional-js
cd functional-js
npm init
```
<!-- .element: class="fragment fade-up" -->

<!-- s -->

![npm-init-2](images/0-setup-npm-2.gif)

<!-- s -->

### ES6 support with babel

- Currently node JS does not support ES6 Javascript code syntax. (e.g. chrome supports it natively)<!-- .element: class="fragment fade-up" -->
- therefore we need to install an npm package:<!-- .element: class="fragment fade-up" -->

`npm install --save @babel/core @babel/node @babel/preset-env`<!-- .element: class="fragment fade-up" -->

<!-- s -->

![babel](images/0-setup-babel.gif)

<!-- s -->

### Editor

- You can use the editor of your choice with JS syntax support but we recommend:<!-- .element: class="fragment fade-up" -->

![VS Code](images/visual-studio-code-logo.png)<!-- .element: class="fragment fade-up" -->

[Download Visual Studio Code](https://code.visualstudio.com/)<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Hello World "normal JS"

- open the folder you created in your editor<!-- .element: class="fragment fade-up" -->
- Create a file called « hello-world.js » and type:<!-- .element: class="fragment fade-up" -->

```javascript
function hello(name) {
    console.log("Hello " + name);
}

hello("Grogu");
```
<!-- .element: class="fragment fade-up" -->

- save the file<!-- .element: class="fragment fade-up" -->
- now open the Terminal inside Visual Studio Code in the menu bar with: >Terminal >Open Terminal<!-- .element: class="fragment fade-up" -->
- Type: <!-- .element: class="fragment fade-up" -->

`node hello-world.js`<!-- .element: class="fragment fade-up" -->

<!-- s -->

![hello world](images/0-hello-world.gif)

- This is with normal Javascript syntax

<!-- s -->

### Hello World "ES6 syntax - arrow functions"

- Create a file called « hello-world-arrow.js » and type:<!-- .element: class="fragment fade-up" -->

```javascript
const hello = name => console.log(`Hello ${name}`)

hello('Grogu');
```
<!-- .element: class="fragment fade-up" -->

- save the file<!-- .element: class="fragment fade-up" -->
- now open the Terminal inside Visual Studio Code in the menu bar with: >Terminal >Open Terminal<!-- .element: class="fragment fade-up" -->
- Then type: « npx babel-node hello-world-arrow.js »<!-- .element: class="fragment fade-up" -->

<!-- s -->

![hello world arrow functions](images/0-setup-hello-world-arrow.gif)

- as node.js does not support ES6 arrow function syntax, it will now be translated for us transparently.