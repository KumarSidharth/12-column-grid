# ![12-column-grid](https://i.ibb.co/zrWLJh3/image.png)

[![GitHub file size in bytes](https://img.shields.io/github/size/kumarsidharth/12-column-grid/dist/grid.min.css?label=minified%20size)](https://github.com/KumarSidharth/12-column-grid/blob/master/dist/grid.min.css)
[![npm](https://img.shields.io/npm/dt/12-column-grid?label=npm%20downloads)](https://www.npmjs.com/package/12-column-grid)
[![jsDeliver hits per month](https://data.jsdelivr.com/v1/package/npm/12-column-grid/badge?style=rounded)](https://www.jsdelivr.com/package/npm/12-column-grid)
[![GitHub issues](https://img.shields.io/github/issues/kumarsidharth/12-column-grid)](https://github.com/KumarSidharth/12-column-grid/issues)
[![GitHub](https://img.shields.io/github/license/kumarsidharth/12-column-grid?color=%23800080)](https://github.com/KumarSidharth/12-column-grid/blob/master/LICENSE)
![GitHub package.json version](https://img.shields.io/github/package-json/v/kumarsidharth/12-column-grid)
![Dependencies](https://img.shields.io/badge/dependencies-0-yellowgreen)
[![GitHub last commit](https://img.shields.io/github/last-commit/kumarsidharth/12-column-grid)](https://github.com/KumarSidharth/12-column-grid/graphs/commit-activity)

* Creates 12 column responsive grid layout
* Customizable
* Light weight
* Zero production dependency
* Class names are same as that of bootstrap
* SCSS Source code
* Uses `display:grid`

## Contents

* Using
  * Adding To Project
    * CDN
    * Installing locally
  * Using Classes
    * `col` classes
    * `d-**-none` classes
    * Aligning grid
  * Examples
    * Responsive list of cards
    * Responsive horizontal navigation links
  * Customizing grids
* Reporting Issues
* Contributing
  * Getting Started
  * Scripts
  * Tasks

## Using

### Adding To Project

#### CDN

```html
<link rel="stylesheet"
      type="text/css"
      href="https://cdn.jsdelivr.net/npm/12-column-grid/dist/grid.min.css">
```

Another CDN

```html
<link rel="stylesheet"
      type="text/css"
      href="https://unpkg.com/12-column-grid/dist/grid.min.css">
```

#### Installing locally

`npm i 12-column-grid`

or

`yarn add 12-column-grid`

To use grids from `node_modules` -

* If your project is using SCSS, import `grid.scss` from `node_modules/12-column-grid/src/grid.scss`.

* Projects without CSS pre-processors or other CSS pre-processors can use minified `grid.min.css` file from `node_modules/12-column-grid/dist/grid.min.css`.

* For unminified file, use `grid.css` from `node_modules/12-column-grid/dist/grid.css`

* Angular projects can import the library using angular.json file. Find the assets array in angular.json and put the path to `node_modules/12-column-grid/src/grid.scss`

    ```json
    {
        "projects": {
            "<Project Name>": {
                "architect": {
                    "build": {
                        "options": {
                            "assets": [
                                "./node_modules/12-column-grid/src/grid.scss"
                            ],
                        },
                    },
                },
            },
        },
    }
    ```

### Using Classes✨

All the class names in this library are same as bootstrap.

The container of the grid items should have a CSS class `row` or `grid`.

The width of the grid is divided into 12 columns.

The screen sizes are divided as

| Screen type        | code | screen width      |
|--------------------|------|-------------------|
| 📽️ extra large screen | xl   | more than 1200px  |
| 🖥️ large screen       | lg   | more than 992px   |
| 💻 medium screen    | md   | more than 768px   |
| 📱 small screen    | sm   | more than 576px   |
| 📟 extra small screen | xs   | less than 576px   |

#### `col` classes

Use the following classes for responsive grid layout

* `col-xl-1, col-xl-2, ... col-xl-12`

* `col-lg-1, col-lg-2, ... col-lg-12`

* `col-md-1, col-md-2, ... col-md-12`

* `col-sm-1, col-sm-2, ... col-sm-12`

* `col-xs-1, col-xs-2, ... col-xs-12`

Mix classes of different screen sizes to get responsive layout

For non-responsive grids use the classes `col-1, col-2, col-3, ... col-12`.

#### `d-**-none` classes

Use the following classes to hide the element for a screen size.

`d-xl-none, d-lg-none, d-md-none, d-sm-none, d-xs-none`

#### Aligning grid

Alignment classes can align the grid or the item. When applied to grid item, it aligns the grid item. When applied to the grid, it aligns the grid itself.

For aligning use the classes

* `align-top` - align at the top
* `align-bottom` - align to the bottom
* `align-right` - align to the right
* `align-left` - align to the left
* `align-h-center` - align the grid horizontally center
* `align-v-center` - align the grid vertically center
* `align-h-stretch` - stretchs the grid horizontally
* `align-v-center` - stretchs the grid vertically

### Examples

#### Responsive list of cards

```html
<div class="row">
    <div class="col-xl-2 col-lg-3 col-md-4 col-sm-6 col-xs-12">
        <img src="https://www.imageurl.com/image">
        <h4>image description</h4>
    </div>
</div>
```

#### Responsive horizontal navigation links

```html
<head>
    <style>
    nav>ul {
        list-style: none;
    }
    </style>
</head>
<body>
<nav>
    <ul class="row">
        <li class="col-md-3 col-sm-12">
            <a href="#">Link 1</a>
        </li>
        <li class="col-md-3 col-sm-12">
            <a href="#">Link 2</a>
        </li>
        <li class="col-md-3 col-sm-12">
            <a href="#">Link 3</a>
        </li>
        <li class="col-md-3 col-sm-12">
            <a href="#">Link 4</a>
        </li>
    </ul>
</nav>
</body>
```

## Customizing grids 🔧

To customise the library, you need to use SCSS in your application.
The following things can be customized -

* Break points

    ```scss
    $breakPoints :(
        xl: 1600px,
        lg: 1200px,
        md: 1080px,
        sm: 480px,
        xs: 0
    );
    ```

    If the keys of `$breakPoints` are changed then it will reflect in the class names generated. For example, if the key `lg` is changed to `large` then the classes `col-lg-1, col-lg-2, ... col-lg-12` will change `col-large-1, col-large-2, ... col-large-12`.

* Number of columns in the grid

    ```scss
    $gridColumns: 10;
    ```

* Gap between the grid rows

    ```scss
    $gridRowGap: 30px;
    ```

* Gap between the grid columns

    ```scss
    $gridColumnGap: 10px;
    ```

* Prefix `.col` before all column clases

    ```scss
    $columnPrefix: '.my-company';
    ```

Use `@import` after declaring variables for customizing.

## Reporting Issues 🆘

Issues for this library can be reported on Github.

[github.com/KumarSidharth/12-column-grid/issues 🔗](https://github.com/KumarSidharth/12-column-grid/issues)

## Contributing 🙋🏻‍♂️

I am looking out for contributers and maintainers for this project. 🖖🏻

### Getting Started 👩‍💻

1. Clone the project in your local machine.

    `git clone https://github.com/KumarSidharth/12-column-grid.git`

2. Make sure you have [Node.js](https://nodejs.org/en/) installed on your machine.

3. Go inside the project folder.

    `cd 12-column-grid`

4. Install dev-dependencies using

    `npm install --only=dev`

This project is meant to have **0 production dependency**.

### Scripts 📜

1. During the development process you can watch the files using

    `npm run watch`

    This script will rebuild the CSS files after every save in SCSS files.

2. Before raising the pull request you should run the script

    `npm run build`

    This script will build the CSS files for production.

### Tasks 📝

|   |Task name                                      |
|---|-----------------------------------------------|
| ⬜️| Add Table of contents in readme               |
| ⬜️| Add Stackblitz link for Usage in Angular      |
| ⬜️| Add codepen / jsFiddle links                  |
| ✅| Add customizable variables                    |
| ✅| Add usage docs                                |
| ⬜️| Add images for result of examples             |
| ✅| Add to CDN                                    |
| ✅| Minify the output file                        |
| ⬜️| Add classes for row-span                      |
| ✅| Hide element on a specific device             |
| ⬜️| Show element on a specific device             |
| ✅| align grid and grid item                      |
| ⬜️| Grid gap based on media queries               |
