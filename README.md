---
title: "Functional programming with Javascript - "
subtitle: "Introduction"
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
  transition: 'slide'
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

# Programming Paradigm

Course of Fontys University of Applied Sciences in Venlo

<!-- s -->

## Objectives

- use major programming paradigms adequately<!-- .element: class="fragment fade-up" -->
- describe their essential characteristics and differences<!-- .element: class="fragment fade-up" -->
- select an appropriate paradigm according to a problem at hand<!-- .element: class="fragment fade-up" -->

<!-- s -->

We use several programming paradigms:

- logical<!-- .element: class="fragment fade-up" -->
- functional<!-- .element: class="fragment fade-up" -->
- object oriented<!-- .element: class="fragment fade-up" -->
- multi-paradigm<!-- .element: class="fragment fade-up" -->

<!-- .slide: data-background="https://media.giphy.com/media/iXTrbbYMQBCMM/giphy.gif" -->


<!-- s -->

## Languages

- Javascript<!-- .element: class="fragment fade-up" -->
- C#<!-- .element: class="fragment fade-up" -->
- Prolog<!-- .element: class="fragment fade-up" -->

<!-- .slide: data-background="https://media.giphy.com/media/3oEjHWbXcpeKhTktXi/giphy.gif" -->

<!-- s -->

## Module description

- [md_ppar.pdf](https://connect.fontys.nl/instituten/fhtenl_studies/studies/INF/PPAR/StudyMaterial/md_ppar.pdf)

<!-- s -->

# Functional programming with Javascript - Introduction

- PPAR - Programming Paradigms course at Fontys Venlo<!-- .element: class="fragment fade-up" -->
- Javascript (modern) + Functional Programming (modern) 🥳<!-- .element: class="fragment fade-up" -->

<!-- n -->
This introduction course is part of a course called PPAR - Programming Paradigms of Fontys University of Applied Sciences. The idea of PPAR is to let students in higher semesters experience different programming paradigms - thus experience what the pros and cons are.
This part covers the functional programming paradigm. For this course was javascript chosen. The reason for that is, that javascript is not only a popular but also a modern programming language. Students can and will use this language also in multiple course - so following this course will not only provide insides into functional programming but - even more important - improve the programming skills in general and with javascript.

Except from module description:

> Being able to decide for an appropiate programming language makes it necessary to have understood different programming paradigms. Only then, one is ale to choose that paradigm which fits most fot a given problem. To this end, this module looks into three important programming paradigms.

<!-- s -->

## Organisational

### Purpose

- The purpose of this workshop as part of the PPAR course is to give a brief introduction of functional programming with javascript by just<!-- .element: class="fragment fade-up" -->

 **doing it**<!-- .element: class="fragment fade-up" -->

- We will use ES6+ as well as node.js<!-- .element: class="fragment fade-up" -->

<!-- n -->

- ES6 stands for ECMAScript version 6 
- European Computer Manufacturers Association (ECMA)

<!-- s -->

### Learning objectives

- The goal of functional programming<!-- .element: class="fragment fade-up" -->
- Declarative vs. imperative programming<!-- .element: class="fragment fade-up" -->
- Ensuring immutability<!-- .element: class="fragment fade-up" -->
- Arrow functions in ES6<!-- .element: class="fragment fade-up" -->
- Passing functions as arguments<!-- .element: class="fragment fade-up" -->
- Mapping, filtering, slicing, sorting, and reducing<!-- .element: class="fragment fade-up" -->
- Advanced functional concepts, currying, recursion<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Course structure

There will be 4 lecturing units where either short lecture or practical work on assignments will take place.<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Exercises

There will be Exercises which can be delivered into an individual Github repository provided by github classroom.<!-- .element: class="fragment fade-up" -->

The invitation link to this exercises will be send during the lecture via mail and as channel-message.<!-- .element: class="fragment fade-up" -->

> Doing the exercises is optional but highly recommended in order to be able to do the assignments<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Assignments

There will be assignments which must be delivered into an individual Github repository provided by github classroom.<!-- .element: class="fragment fade-up" -->

The invitation link to this assignments will be send during the lecture via mail and as channel-message.<!-- .element: class="fragment fade-up" -->

> You have to do and pass all assignments. Doing means pushed into your individual github repository in order to pass the Functional programming part of the PPAR course.<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Grading

- Grading was or will be explained separately. See also connect-webpage for the details: <!-- .element: class="fragment fade-up" -->

[PPAR - Programming paradigms - Connect](https://connect.fontys.nl/instituten/fhtenl_studies/studies/INF/PPAR/)<!-- .element: class="fragment fade-up" -->

<!-- s -->
<!-- .slide: data-background="https://media.giphy.com/media/fQZX2aoRC1Tqw/giphy.gif" -->

Let's go to work 💻
