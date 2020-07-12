# 12-column-grid

* CSS library
* Creates 12 column responsive grid layout
* Customizable
* Light weight
* Zero production dependency
* Class names are same as that of bootstrap
* SCSS Source code
* Uses `display:grid`

## Using

### Adding To Project

Install this library from npm using the command

`npm i 12-column-grid`

* If your project is using SCSS, import `grid.scss` from `node_modules/12-column-grid/src/grid.scss`.

* Projects without CSS pre-processors or other CSS pre-processors can use `grid.css` from `node_modules/12-column-grid/dist/grid.css`

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

### Using Classes

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

Use the following classes for responsive grid layout

* `col-xl-1, col-xl-2, ... col-xl-12`

* `col-lg-1, col-lg-2, ... col-lg-12`

* `col-md-1, col-md-2, ... col-md-12`

* `col-sm-1, col-sm-2, ... col-sm-12`

* `col-xs-1, col-xs-2, ... col-xs-12`

Mix classes of different screen sizes to get responsive layout

For non-responsive grids use the classes `col-1, col-2, col-3, ... col-12`.

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

### Getting Started

1. Clone the project in your local machine.

    `git clone https://github.com/KumarSidharth/12-column-grid.git`

2. Make sure you have [Node.js](https://nodejs.org/en/) installed on your machine.

3. Go inside the project folder.

    `cd 12-column-grid`

4. Install dev-dependencies using

    `npm install --only=dev`

This project is meant to have **0 production dependency**.

### Scripts

1. During the development process you can watch the files using

    `npm run watch`

    This script will rebuild the CSS files after every save in SCSS files.

2. Before raising the pull request you should run the script

    `npm run build`

    This script will build the CSS files for production.

### Tasks

|   |Task name                                      |
|---|-----------------------------------------------|
| ⬜️| Add Stackblitz link for Usage in Angular      |
| ⬜️| Add codepen / jsFiddle links                  |
| ✅| Add customizable variables                    |
| ✅| Add usage docs                                |
| ⬜️| Add images for result of examples             |
| ⬜️| Add to CDN                                    |
| ✅| Minify the output file                        |
| ⬜️| Add classes for row-span                      |
| ⬜️| Show/Hide element on a specific device        |
| ⬜️| align grid and grid item                      |
