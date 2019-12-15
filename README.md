# Learn Webpack : A beginner's guide to Webpack

This repo is a parenthesis on my voyage in the land of NodeJS. In my last repo [webpackexample](https://github.com/OpenTechConsult/webpackexample) where I started to learn Webpack as a front-end build system, I made a huge error probably due to the inconsistency of the versions of webpack and it plugins and loader with my webpack configuration file. I reported the bug [here](https://github.com/OpenTechConsult/webpackexample/issues/2) and I will go back to fix it in a later date.

I decided to start this new repo that illustrate my learning of webpack. I want to start with a clean slate and use a relatively new version of webpack so that I can understand the mistake that I made in my last repo. The article, source of this repo can be found here at [Sitepoint](https://www.sitepoint.com/webpack-beginner-guide/). This article explains relatively well what Webpack is, Webpack's main concept and how Webpack works. We are not going to make another explanation. Rather we are going to directly dive in and start scaffolding a project that use webpack as a front-end build system.

## Getting started

After learning the fundamental concepts and terminologies of webpack, let's do some practice.

To start, let's create a new directory and cd into it. The initialize a new project.

> `mkdir learnwebpack && cd learnwebpack` <br>
> `git init` : if you have git installed, initialize a git repo <br>
> `npm init` : initialize a new project by answering the necessary questions<br>

Next, we need to install webpack and webpack CLI locally

> `npm install webpack webpack-cli --save-dev`

The content of the generated **package.json** should be similar to the following

```json
{
  "name": "learnwebpack",
  "version": "1.0.0",
  "description": "Yet another webpack learning tutorial project.",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/OpenTechConsult/learnwebpack.git"
  },
  "keywords": ["Webpack","Front-end","Build","Node","Npm","Git"],
  "author": "OpenTechConsult",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/OpenTechConsult/learnwebpack/issues"
  },
  "homepage": "https://github.com/OpenTechConsult/learnwebpack#readme",
  "devDependencies": {
    "webpack": "^4.41.2",
    "webpack-cli": "^3.3.10"
  }
}
```

## Create webpack tasks using npm custom scripts

Webpack can also be used as simple task runner. We can create webpack tasks by including the name of our task followed by its instructions in the script section of the package.json file. The ***scripts*** section should look as following

```json
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "webpack --mode development",
    "build": "webpack --mode production"
  }
  ```

  We can reference locally installed npm packages by their name in the scripts property. Here we created two tasks. The first  is called **dev** and it use the webpack tool by calling its name and by add some additional flags to tell to run webpack in development mode.

  The second task called **build** also use webpack tool by calling it name and by using the flag _--mode production_ to signify that it will run in production mode.

  Before we test the tasks, let create a file called **index.js** inside a directory called **src**. Put the following code inside the index.js file `console.log("Hello, webpack");`. Now we can run the **dev** tasks to start webpack in development mode.

  > `npm run dev`

To see if all goes well and we get the correct output, we need to display the result in the browser. We create an `index.html`file in the `dist` folder.

```html
<!doctype html>
<html>
  <head>
    <title>Getting Started</title>
  </head>
  <body>
    <script src="main.js"></script>
  </body>
</html>
```

Now if we open the file in the browser we should see the _Hello Webpack_ message in the console.
  