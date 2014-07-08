grunt-Mustatic
==============

> Grunt task for rendering static HTML templates with [Mustache](http://mustache.github.io/)

## Getting Started
This plugin requires Grunt `~0.4.2`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install dbushell-grunt-mustatic --save
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('dbushell-grunt-mustatic');
```

## The Mustatic Task

### Configuration

Example task configuration:

```js
grunt.initConfig({
    mustatic: {
        options: {
            src: 'templates',
            dest: 'build'
        },
        prod: {
            globals: {
                lang: 'en',
                charset: 'utf-8'
            }
        }
    }
});
```

### Options

#### options.src

Type: `String` default: `"templates"`

This is the source directory of your mustache templates and JSON data. The directory should be structured like so:

```
templates/
    base.html
    base.json
        pages/
            index.html
            index.json
        partials/
            header.html
            footer.html
```

* `base.html` is your root template can should contain at least `{{>content}}`
* `base.json` includes your global data not defined at task configuration
* `pages/` contains templates to be rendered with template specific data
* `partials/` contains partial templates to be included in pages


#### options.dest

Type: `String` default: `"build"`

This is the build directory where rendered HTML files will be saved.

#### options.ext

Type: `String` default: `"html"`

This is the file extension used for your mustache templates.

#### globals

Type: `Object` default: `{ }`

This is global template data in which `base.json` will be merged. These are environment-specific.

* * *

Created by: [David Bushell](http://dbushell.com) | [@dbushell](http://twitter.com/dbushell) (based on: [grunt-mustache-html](https://github.com/haio/grunt-mustache-html))
Using: [Hogan.js](https://github.com/twitter/hogan.js) to compile Mustache templates

Copyright © David Bushell | MIT license
