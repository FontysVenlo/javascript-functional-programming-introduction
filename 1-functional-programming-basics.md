---
title: "Functional programming with Javascript - "
subtitle: "Basics"
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

# Functional Programming - Basics

## What is Functional Programming?

> Functional programming is a programming paradigm a style of building the structure and elements of computer programs that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data -
*Wikipedia*
<!-- .element: class="fragment fade-up" -->

<!-- s -->

- Functional programming is<!-- .element: class="fragment fade-up" -->
  - a programming paradigma<!-- .element: class="fragment fade-up" -->
  - mathematical functions<!-- .element: class="fragment fade-up" -->
  - avoids changing-state<!-- .element: class="fragment fade-up" -->
  - avoids mutable data<!-- .element: class="fragment fade-up" -->

<!-- s -->

## What is a function?

- Function has inputs and an output<!-- .element: class="fragment fade-up" -->

![Inputs and Outputs](images/input-output1.png)<!-- .element: class="fragment fade-up" -->

<!-- s -->

- Output (result) depends on the inputs (parameters)<!-- .element: class="fragment fade-up" -->
Simple example: <!-- .element: class="fragment fade-up" -->

![Simple example](images/input-output2.png)<!-- .element: class="fragment fade-up" -->

- 12 and 34 are inputs <!-- .element: class="fragment fade-up" -->
- the function sums (+)<!-- .element: class="fragment fade-up" -->
- 46 is the output<!-- .element: class="fragment fade-up" -->

<!-- s -->

Another example:

![Input and Output other example](images/input-output3.png)<!-- .element: class="fragment fade-up" -->

- a geometric object and 2 are inputs<!-- .element: class="fragment fade-up" -->
- the function is scaling<!-- .element: class="fragment fade-up" -->
- the output is a geometric object<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Why Functional Programming?

- Object-oriented programming languages<!-- .element: class="fragment fade-up" -->
  - Java<!-- .element: class="fragment fade-up" -->
  - C++<!-- .element: class="fragment fade-up" -->
  - C#<!-- .element: class="fragment fade-up" -->
- difficult bug fixing<!-- .element: class="fragment fade-up" -->
- in enterprise usually thousands of variables<!-- .element: class="fragment fade-up" -->
- apps get into buggy state<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Functional Programming

- uses some techniques to avoid buggy states<!-- .element: class="fragment fade-up" -->
  - smaller parts<!-- .element: class="fragment fade-up" -->
  - self-contained parts<!-- .element: class="fragment fade-up" -->
  - easily testable parts<!-- .element: class="fragment fade-up" -->
  - easily modifiable parts<!-- .element: class="fragment fade-up" -->

<!-- n -->

- Object-oriented languages also try to organize the code in smaller, self-contained parts so that the code gets more easily testable and modifiable. However, often the success rate is not so high. 
- So Functional Programming offers some other techniques for reaching that goal. By the way, most modern OO-languages also introduced functional programming (e.g. Java)

<!-- s -->

### Imperative vs Declarative

- What does a car consists of?<!-- .element: class="fragment fade-up" -->

vs.<!-- .element: class="fragment fade-up" -->

- How do I build a car?<!-- .element: class="fragment fade-up" -->

<!-- s -->

### How vs What

Imperative: HOW?<!-- .element: class="fragment fade-up" -->

Declarative: WHAT?<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Imperative "HOW" example

> Sum of an array of numbers<!-- .element: class="fragment fade-up" -->

- Set x to zero<!-- .element: class="fragment fade-up" -->
- Add the first number in the array to x<!-- .element: class="fragment fade-up" -->
- Repeat previous step for the rest of the numbers in the array<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Declarative "WHAT" example

> Sum of an array of numbers<!-- .element: class="fragment fade-up" -->

- X is the sum of all the numbers in the array<!-- .element: class="fragment fade-up" -->

🤔<!-- .element: class="fragment fade-up" -->

<!-- s -->

## Core Concepts of Functional Programming

- Immutability<!-- .element: class="fragment fade-up" -->
- Separating functions and data<!-- .element: class="fragment fade-up" -->
- First-class functions<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Immutability

**Java**<!-- .element: class="fragment fade-up" -->

```java
int x = 10; // initialize variable 
System.out.println(x); // prints 10

x = 100; // change value
System.out.println(x); // prints 100

x = -1; // change value again
System.out.println(x); // prints -1
```
<!-- .element: class="fragment fade-up" -->

**Javascript**<!-- .element: class="fragment fade-up" -->

```javascript
var x = 10; // initialize variable 
console.log(x); // prints 10

x = 100; // change value
console.log(x); // prints 100

x = -1; // change value again
console.log(x); // prints -1
```
<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Immutability in javascript

```javascript
var x = 10; // instead of var
let y = 10; // or let
```
<!-- .element: class="fragment fade-up" -->

```javascript
const x = 10; // use const keyword
```
<!-- .element: class="fragment fade-up" -->

`const`<!-- .element: class="fragment fade-up" -->

- keyword defines a constant which cannot be changed<!-- .element: class="fragment fade-up" -->

- In Java: <!-- .element: class="fragment fade-up" -->

`final`<!-- .element: class="fragment fade-up" -->

- variables cannot be changed!!!<!-- .element: class="fragment fade-up" -->

<!-- s -->

🤔

`x = 3` <!-- .element: class="fragment fade-up" -->

- literally means that x is 3<!-- .element: class="fragment fade-up" -->
- In OO you usually say that x is a container which can hold a value.<!-- .element: class="fragment fade-up" -->

`const pi = 3.14159` <!-- .element: class="fragment fade-up" -->

- literally means that pi is 3.14159<!-- .element: class="fragment fade-up" -->
- functional programming treats all values as constant (such as pi)<!-- .element: class="fragment fade-up" -->

- ➡ Never change a running sys... ehm initialized variable<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Examples

#### Java<!-- .element: class="fragment fade-up" -->

```java
Employee employee1 = new Employee('Elon Musk', 70000);
employee1.raiseSalary (10000000000);
```
<!-- .element: class="fragment fade-up" -->

#### Javascript immutable example<!-- .element: class="fragment fade-up" -->

```javascript
const employee1 = {
  name: 'Elon Musk',
  salary: 70000,
};

const updatedEmployee1 = {
  name: employee1.name,
  salary: employee1.salary + 10000000000,
};

```
<!-- .element: class="fragment fade-up" -->

<!-- n -->

- Advantage is that we do not have to handle state changes.
- No change of reference variables like in other languages.
- e.g. in Java, passed by reference parameters!!! If you change the value of the passed parameter, you change the whole reference variable.
- Btw. to be fair, there are best practices in OO languages like Java to prevent this unwanted/unsecure behaviour, e.g. use unmodifiable Collections, make copies of variables and so forth.
- Generally, mutable variables can and often will lead to unwanted behaviour and bugs in your program.


<!-- s -->

## Separation of Data and Functions

### Data (as JSON)<!-- .element: class="fragment fade-up" -->

```javascript
  {
    "id": 43,
    "name": "OBAMA B",
    "birth_year": 1961,
    "years_served": 8,
    "party": "DEMOCRATIC",
  },
  {
    "id": 44,
    "name": "TRUMP D J",
    "birth_year": 1946,
    "years_served": 0,
    "party": "REPUBLICAN",
  }
```
<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Even more data

```javascript
  {
    "pres_id": 43,
    "spouse_name": "ROBINSON M",
    "spouse_age": 28,
    "nr_children": 2,
    "marriage_year": 1992
  },
  {
    "pres_id": 44,
    "spouse_name": "ZELNICKOVA I",
    "spouse_age": 28,
    "nr_children": 3,
    "marriage_year": 1977
  },
```
<!-- .element: class="fragment fade-up" -->

<!-- s -->

> Data in Functional Programming is represented as simple arrays and hashes or (javascript) objects

<!-- s -->

### Functions

#### In object orientation<!-- .element: class="fragment fade-up" -->

**Java**<!-- .element: class="fragment fade-up" -->

```java
public class President {
  
  private String name;
  private int birth_year;
  private Spouse[] spouses;

  // ...

  public int getNumberOfSpouses() {   
      // ... 
  }
}
```
<!-- .element: class="fragment fade-up" -->

<!-- n -->

- Functions or methods are along with the data they belong to - inside classes.
- makes it easy to access as everything is in place

<!-- s -->

#### In functional programming

**Javascript**<!-- .element: class="fragment fade-up" -->

```javascript
const presidentsArray = [ ... ];

const spousesArray = [ ... ];

const findNumberOfSpouses = (president, spouses) => ({
    // ...
});

const numberOfSpouses = 
  findNumberOfSpouses(presidentsArray[41], spousesArray);
```
<!-- .element: class="fragment fade-up" -->

- functions and data separated<!-- .element: class="fragment fade-up" -->
- functions do not (cannot) change the data<!-- .element: class="fragment fade-up" -->
- functions return new data objects<!-- .element: class="fragment fade-up" -->

<!-- s -->

## First-class functions

> In computer science, a programming language is said to have first-class functions if it treats functions as first-class citizens. This means the language supports passing functions as arguments to other functions, returning them as the values from other functions, and assigning them to variables or storing them in data structures. - Wikipedia <!-- .element: class="fragment fade-up" -->

- In short, you can use functions as parameters and return values.<!-- .element: class="fragment fade-up" -->
- You can create arrays of functions<!-- .element: class="fragment fade-up" -->

<!-- s -->

### Example

```javascript
const arrayOfFunctions = [
   function doThis() { /* ... */ },
   function soThat() { /* ... */ },
];

doSomething(function sayHello() { /* ... */ });

// this is the non-arrow syntax of defining a function 
function giveMeAFunction() {
  return function() {
    console.log('I am a function');
  }
}
```
<!-- .element: class="fragment fade-up" -->

<!-- s -->

## Some issues

- Javascript perfectly suits well for using functional programming 💪<!-- .element: class="fragment fade-up" -->
- However, Javascript is not a PURE functional programming language, like e.g. Haskell 😢<!-- .element: class="fragment fade-up" -->
- E.g. constants work well but do not totally ensure immutability, see: 🐛<!-- .element: class="fragment fade-up" -->0


<!-- s -->

![Immutability issue](images/1-immutability-issue.jpg)

<!-- s -->

## Solution

- ESLint. We do not go into details, if you are interested:<!-- .element: class="fragment fade-up" -->

[jhusain/eslint-plugin-immutable: ESLint plugin to disable all mutation in JavaScript.](https://github.com/jhusain/eslint-plugin-immutable)<!-- .element: class="fragment fade-up" -->

- For more information see: <!-- .element: class="fragment fade-up" -->

[ESLint - Pluggable JavaScript linter](https://eslint.org/)<!-- .element: class="fragment fade-up" -->