# Learn Webpack : A beginner's guide to Webpack

This repo is a parenthesis on my voyage in the land of NodeJS. In my last repo [webpackexample](https://github.com/OpenTechConsult/webpackexample) where I started to learn Webpack as a front-end build system, I made a huge error probably due to the inconsistency of the versions of webpack and it plugins and loader with my webpack configuration file. I reported the bug [here](https://github.com/OpenTechConsult/webpackexample/issues/2) and I will go back to fix it in a later date.

I decided to start this new repo that illustrate my learning of webpack. I want to start with a clean slate and use a relatively new version of webpack so that I can understand the mistake that I made in my last repo. The article, source of this repo can be found here at [Sitepoint](https://www.sitepoint.com/webpack-beginner-guide/). This article explains relatively well what Webpack is, Webpack's main concept and how Webpack works. We are not going to make another explanation. Rather we are going to directly dive in and start scaffolding a project that use webpack as a front-end build system.

## Getting started

After learning the fundamental concepts and terminologies of webpack, let's do some practice.

To start, let's create a new directory and cd into it. The initialize a new project.

> `mkdir learnwebpack && cd learnwebpack`
> `git init` : if you have git installed, initialize a git repo
> `npm init` : initialize a new project by answering the necessary questions

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