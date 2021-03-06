# express-debug
express-debug is a development tool for expressjs. It's simple middleware that
injects useful debugging output into your html, in a non-obstructive way.

It adds an 'EDT' tab to the right side of pages that, when clicked, displays info
such as template variables (locals), current session, useful request data, and
current template.

express-debug should *NOT* be used in production environments.

Compatible with express 3.x


### Settings

__depth:__ How deep to recurse through printed objects. (Default: 4)


### Usage

#### Install
`npm install express-debug --save-dev`

#### Use
```js
var express = require('express');
var app = express();

/* you are using different environments, right? =) */
app.configure('development', function() {
    var edt = require('express-debug');

    app.use(edt({/* settings */}));
})

/* ... application logic ... */
```


### Issues
Pull requests, feature requests, bug reports, and style breakage reports welcome!


### Changelog
* **0.1.2**
    * objects can now be collapsed
    * functions are now collapsed by default, showing only # of formal args and name, but can be expanded
    * separated css and js from main toolbar template

* **0.1.1**
    * remove environment checks
    * fix "view engine" directive, make template reading safer


### Goals for 0.2.0
* Cleaner/modular project structure
* Pluggable panels


### License - MIT
Copyright (c) 2013 Tom Hunkapiller and contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
