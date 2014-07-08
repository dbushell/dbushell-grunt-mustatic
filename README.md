grunt-Mustatic
==============

> Grunt task for rendering static HTML templates with Mustache

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
            src  : 'templates',
            dest : 'build'
        },
        prod: {
            globals: {
                lang    : 'en',
                charset : 'utf-8'
            }
        }
    }
});
```

### Options

#### options.src

Type: `string` (default: `templates`)

This is the source directory of your mustache templates and data.

#### options.dest

Type: `string` (default: `build`)

This is the build directory where your rendered HTML files are saved.

* * *

Created by: [David Bushell](http://dbushell.com) | [@dbushell](http://twitter.com/dbushell) (based on: [grunt-mustache-html](https://github.com/haio/grunt-mustache-html))

Copyright © David Bushell | MIT license
