eventListenerPolyfill
=====================
IE6-IE8 Polyfill for missing `addEventListener` and `removeEventListener` Javascript methods.

This Polyfill allows a standard way for most browsers to manage event listeners. The lack of standard implementation makes  tasks such as executing Javascript after a page is loaded difficult. This Polyfill relies on IE6-IE8's `attachEvent` and `detectEvent` which is why it only works for these browsers.

This project origins from :

 * https://gist.github.com/2864711/946225eb3822c203e8d6218095d888aac5e1748e (original proposal/idea)
 * http://qiita.com/sounisi5011/items/a8fc80e075e4f767b79a#11 (2014 remake)

The second version has not had a lot visibility given it was hosted on a Japanese website. This repository has been setup so that more people can contribute to this Polyfill.

_This script is stand alone and does not required any external library._

### Size

- Full version: 5k 
- Minified: 1.2k
- Minified & Compressed: 0.8k

### Supports
 - Browsers: IE6-IE8 (all other browsers will ignore the script)
 - Scope: useCapture is not supported when using the Polyfill
 - Limitations: Could potentially not play nice with JQuery and other scripts with similar features.

### Usage

Simply load this script in your HTML code and use the `addEventListener` and `removeEventListener` methods.

Example

1) Add the script on your page

	<script src="js/addEventListenerIEPolyfill.js"></script>

2) Try your new methods on old browsers:

    // Example with an object.
    var helloWorld = function () {alert('hello world');};
    window.addEventListener('load', helloWorld);
    
    // Example passing an argument.
    var say = function (something) {alert('You said ' + something);};
    window.addEventListener('load', function () {say('hello world')});

3) You're done
