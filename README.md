es6-self
========
__Using "self" in classes in a consistent way. An important, particularly useful feature for ECMAScript 6.__

Template
--------
```javascript
const self = class Class {
    constructor() {}
};

export default self;
```
Example
-------
```javascript
const self = class Color {
    static fromStringToRGB(string = "0") {
        return parseInt(string);
    }
    constructor() {
        this._rgb = 0x000000;
    }
    parseString(string) {
        /* Using "self" to invoke a static function
           (in this case .fromStringToRGB()) rather
           than call Color.fromStringToRGB(string) */
        this._rgb = self.fromStringToRGB(string);
    }
};

export default self;
```
Suggestions, Ideas & Requests
-----------------------------
Post any occurring suggestions, useful ideas and requests to the project's issue page under the __suggestion/idea/request__ label by clicking [here](https://github.com/richard-kng/es6-self/labels/suggestion/idea/request).

 - Constructive criticism is encouraged and welcomed by contacting the developer or using GitHub.

Issues/Bugs
-----------
In case of any occurring issues and/or bugs, post on the project's [issues](https://github.com/richard-kng/es6-self/issues) page with appropriate label(s).

Support
-------
If you find this tool useful, you can support this project by supporting the developer [here](http://richard-kng.github.io/support/).

Contribution & A Note
---------------------
In the spirit of open source software development, this project is always open to and encourages community code contribution. To get started, just run through the source file, check the comments and general coding style and start to contribute.

- In case you find this GitHub repository useful, [support it](http://richard-kng.github.io/support/) by supporting the developer, follow the developer on [social platforms](http://richard-kng.github.io/support/#social) or send an email to the developer.

License
-------
Copyright (c) 2014 "Richard KnG" Richárd Szakács. __Licensed under the MIT license__.

The license mentioned above applies to all parts of this software except as
documented below

All files located in the node_modules and external directories are
externally maintained libraries used by this software which have their
own licenses. We recommend you read them, as their terms may differ from
the terms above.
