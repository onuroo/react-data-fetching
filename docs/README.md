<div align="center">
  <a href="https://github.com/CharlesMangwa/react-data-fetching" target="\_parent">
    <img 
      alt="React Data Fetching logo"
      src="images/logo.png"
      width="900"
    />
  </a>
</div>
<div align="center">
  <br />
  <a href="https://circleci.com/gh/CharlesMangwa/react-data-fetching">
    <img
      alt="build: CircleCI"
      src="https://circleci.com/gh/CharlesMangwa/react-data-fetching.svg?style=shield&circle-token=ec4d3afecb3cd2d7fd6712b2a6b2f576b9dfb08f"
    />
  </a>
  <a href="https://coveralls.io/github/CharlesMangwa/react-data-fetching?branch=master">
    <img
      alt="coverage: Coveralls"
      src="https://coveralls.io/repos/github/CharlesMangwa/react-data-fetching/badge.svg?branch=master&t=v4mvo8"
    />
  </a>
  <a href="https://www.npmjs.com/package/react-data-fetching">
    <img
      alt="version: 0.1.1"
      src="https://img.shields.io/npm/v/react-data-fetching.svg"
    />
  </a>
  <img 
    alt="gzip size"
    src="https://img.shields.io/badge/gzip%20size-4.04%20kB-brightgreen.svg"
  />
  <img
    alt="module formats: umd, cjs, esm"
    src="https://img.shields.io/badge/module%20formats-umd%2C%20cjs%2C%20esm-green.svg"
  />
  <a href="https://github.com/CharlesMangwa/react-data-fetching/pulls">
    <img
      alt="PRs welcome"
      src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"
    />
  </a>
</div>

`react-data-fetching` provides a very intuitive way to perform any REST API call without hassle, through a single React component. It also helps you take care of timeouts, loading states, errors handling, data saving, uploading/downloading progress, etc. Fetching data while letting the user know what's going on has never been that easy!

The package is really lightweight (~4 kB gzipped) and has been built from the ground up with universal apps in mind: you can use it wherever React is rendering - meaning it works seamlessly with React (web) & React Native!


## Installation

Using [Yarn](https://yarnpkg.com/):

```shell
$ yarn add react-data-fetching
```

Then, use it as you would with anything else:

```js
// using ES6 modules
import { Fetch } from "react-data-fetching"

// using CommonJS modules
var Fetch = require("react-data-fetching").Fetch
```

The UMD build is also available on [unpkg](https://unpkg.com):

```html
<script src="https://unpkg.com/react-data-fetching/umd/react-data-fetching.min.js"></script>
```

You can find the library on `window.ReactDataFetching`.

## Usage

The following illustrates the simplest way to use `react-data-fetching`:

```jsx
import React, { Component } from "react"
import { Fetch } from "react-data-fetching"

import { Loader } from './components'

export default class App extends Component {
  render() {
    return (
      <Fetch
        loader={<Loader/>} // Replace this with your lovely handcrafted loader
        url="https://api.github.com/users/octocat"
        timeout={5000}
      >
        {({ data }) => (
         <div>
          <h1>Username</h1>
          <p>{data.name}</p>
         </div>
        )}
      </Fetch>
    )
  }
}
```

The package gives  access to `<Fetch>`, `<ConnectedFetch>` and `requestToApi()`. To have an in-depth explanation of how to use them, how they work and even more, head to this post: [Introducing 🎣 React Data Fetching](https://medium.com/p/2140a1d36cc8/).

## About

`react-data-fetching` is currently developed and maintained by yours truly, [@Charles_Mangwa](https://twitter.com/Charles_Mangwa). Feel free to get in touch if you want to contribute!
