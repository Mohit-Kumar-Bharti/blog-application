---
title: "Babel transpiler"
date: "December 22, 2021"
excerpt: "Babel is a JavaScript transpiler that converts edge JavaScript(ES6) into plain old ES5 JavaScript that can run in any browser even in the old ones"
cover_image: "/images/posts/babel.png"
category: "JavaScript"
author: "Mohit Kumar"
author_image: "/images/profile.jpeg"
---

## What is Babel?

Babel is a JavaScript [transpiler](https://learnwithharsh.me/blog/transpile-in-javascript) that converts edge JavaScript(ES6) into plain old ES5 JavaScript that can run in any browser even in the old ones. It can [transpile](https://learnwithharsh.me/blog/transpile-in-javascript) every new syntax code to old similar code which is supported by every browsers.

## Reason for using Babel

The biggest reason behind using _Babel_ is that all the latest features of javascript are not supported in every browser yet. Hence, someone needs to do the converting part. And here comes Babel, which transpile latest ES6 features to ES5 features which is understandable by every browser.

## Setting up Babel into our project

- Babel comes as a package as a node module which can be installed via npm (node package manager).

> Step 1

Create the directory of your project where we are going to test babel in action. I've created mine as _Babel-testing_

> Step 2

Change the directory to _Bable-testing_

> Step 3

Initialize your repository with npm with code given

```js
    npm init -y
```

This will create a <code>package.json</code> file.

> Step 4

Install babel core and babel cli by executing the code given

```js
    npm install --save-dev @babel/core @babel/cli
```

> Step 5

Create a folder named _src_ in the root of your directory. This src folder will contain all your code that is needed to be transpiled.<br>
Go to the <code>package.json</code> file and replace your <code>script object with below code</code>

```js
    "scripts" : {
        "build" : "babel src -d dest"
    }
```

The above build command will take each and every file present in **src** folder and then transpile it and finally put transpiled files to the destination folder - **dest**

> Step 6

Create a file named _script.js_ in your _src_ folder and write some code. Below is the example of code you can use:

```js
const a = [1, 2, 3];
console.log(...a);
```

> Step 7

Install a preset package of babel by executing below code.

```js
    npm install @babel/preset-env --save-dev
```

> Step 8

Create a file named _babel.config.json_ in the root of your directory which will tell the babel what we want to do (here transpile). Write the below code to the same file:

```js
{
  presets: ["@babel/preset-env"];
}
```

> Step 9

Phew! We have done so many work but haven't got the result what we are trying to do. So it's time to get exact transpiled code as a result to this messy work. For this, execute the code given

```js
    npm run build
```

> Step 10

Finally, we have done it! All the files present inside src folder get transpiled and it can be visible in _dest_ folder that have been created by **Babel**. <br>

You can write anything inside the file in _src_ folder and babel will transpile it and send the output in _dest_ folder.

For now, your code in *dext/script.js*should like :

```js
"use strict";

var _console;

var a = [1, 2, 3];

(_console = console).log.apply(_console, a);
```

## Summary

We have successfully done the setup of babel in our repository.

Hope you have enjoyed and gained some knowlegdge.

**Contributer** : [Harsh Anand](https://github.com/its-me-Harsh-Anand)
