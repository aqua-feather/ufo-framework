
# UFO Framework 
###### Based of framework by [DesignByCodeCode]('https://www.npmjs.com/package/hoodoo-sass') 

This is a very light weight css framework with only the bear minimal to create a response website layout. This framework only consist of 3 major components. 
A customizable responsive grid, some buttons and form elements. 

## Index 

- [Installation](#installation)
- [Setup framework](#setup-framework)
- [Override defaults](#override-defaults)
- [How to use](#how-to-use)
    - [Grid](#the-grid)
    - [Buttons](#the-buttons)
    - [Extend settings](#extend-settings)

## Installation
UFO Framework can be installed with npm or yarn 
```bash
npm install ufo-framework
```

```bash
yarn add ufo-framework
```

## Setup Framework
The framework is created using scss. To use it you need to set up you sass environment first. Create your main sass/scss file and add the following two 
lines of code to the file.

```scss
@import "~ufo-framework/src/scss/settings";
@import "~ufo-framework/src/scss/init";
```

## Override defaults
To override the default colors and grid sizes you only need to create a _settings.scss file in your project main sass/scss folder and coping the following code in to it.

Now you can override the theme colors and grid sizes to your need

> Please note that you can change the key as well as the value of the color and grid.

```scss
$max-width: 1200px;
$column-count: 12;
$screen-sizes: (
    'small': 300px,
    'medium': 800px,
    'large': 1100px,
);
$padding : 10px;
$colors: (
    dark: #1c0b19,
    medium-dark: #140d4f,
    medium: #4ea699,
    light: #25e491,
    very-light: #ddf9ea,
    success: #7ac74f,
    info: #25ced1,
    warning: #f75c03,
    alert: #dc143c,
)
```

## How to use
> The follow code is working with the default settings file. Just alter the prefix to you corresponding key value name for grid sizes and colors. 

### The Grid
```html
<div class="container">
    <div class="row">
        <div class="small-col-6 medium-col-4"></div>
        <div class="small-col-6 medium-col-4"></div>
        <div class="small-col-12 medium-col-4"></div>
    </div>
</div>
```

### The Buttons
You can create button with any of the $colors map key value
```html
<a href="#" class="button button--dark">Dark Button</a>
<a href="#" class="button button--medium-dark">Medium Dark Button</a>
<a href="#" class="button button--medium">Medium Button</a>
.....
<a href="#" class="button button--info">Info Button</a>
<a href="#" class="button button--success">Success Button</a>
<a href="#" class="button button--warning">Warning Button</a>
<a href="#" class="button button--alert">Alert Button</a>
```

### Extend settings
There is no limit to how many colors that can be added to the $colors map in _settings file. The same is true of the grid. you can swap the key name with 
your own and add or remove the key value pair you don't want. 

```scss
$screen-sizes: (
    'small': 300px,
    'medium': 800px,
    'large': 1100px,
);
// Change to 
$screen-sizes: (
    'xs': 300px,
    's': 400px,
    'm': 800px,
    'l': 1100px,
    'xl': 1200px,
);
```
```scss
$colors: (
    dark: #1c0b19,
    medium-dark: #140d4f,
    medium: #4ea699,
    light: #25e491,
    very-light: #ddf9ea,
    success: #7ac74f,
    info: #25ced1,
    warning: #f75c03,
    alert: #dc143c,
);
// Change to
$colors: (
    main: #1c0b19,
    secondary: #140d4f,
    success: #7ac74f,
    info: #25ced1,
    warning: #f75c03,
    alert: #dc143c,
);
```


## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits
- [Renier Grobler](https://github.com/aque-feather)
- [Claude Myburgh](https://github.com/designbycode)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
