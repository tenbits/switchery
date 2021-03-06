![Switchery](http://i.imgur.com/xJAM3Jq.png)

## Description

Switchery is a simple component that helps you turn your default HTML checkbox inputs into beautiful iOS 7 style switches in just few simple steps. You can easily customize switches, so that they match your design perfectly.

Supported by all modern browsers: Chrome, Firefox, Opera, Safari, IE8+

![Preview](http://i.imgur.com/0PcuTbO.jpg)

[Live Preview](http://abpetkov.github.io/switchery/)

## Installation

##### Standalone:

```html
<link rel="stylesheet" href="dist/switchery.css" />
<script src="dist/switchery.js"></script>
```

##### Component:

```shell
$ component install abpetkov/switchery
```

##### Bower:

```shell
$ bower install switchery
```

## Usage

```js
var elem = document.querySelector('.js-switch');
var init = new Switchery(elem);
```

Use the above for the standalone version. For development you need `var Switchery = require('switchery');` at the very beginning.

## Settings and Defaults

```js
defaults = {
    color          : '#64bd63'
  , secondaryColor : '#dfdfdf'
  , className      : 'switchery'
  , disabled       : false
  , disabledOpacity: 0.5
  , speed          : '0.4s'
};
```

- `color` : color of the switch element (HEX or RGB value)
- `secondaryColor` : secondary color for the box shadow and border, when the switch is off
- `className` : class name for the switch element (by default styled in switchery.css)
- `disabled` : enable or disable click events and changing the state of the switch (boolean value)
- `disabledOpacity` : opacity of the switch when it's disabled (0 to 1)
- `speed` : length of time that the transition will take, ex. '0.4s', '1s', '2.2s' (Note: transition speed of the handle is twice shorter)

## Examples

##### Checked

Only thing you need is to add a `checked` attribute to your checkbox input. Simple as that.

```html
<input type="checkbox" class="js-switch" checked />
```

##### Multiple switches

You can add as many switches as you like, as long as their corresponding checkboxes have the same class. Select them and make new instance of the Switchery class for every of them.

```js
var elems = Array.prototype.slice.call(document.querySelectorAll('.js-switch'));

elems.forEach(function(html) {
  var switchery = new Switchery(html);
});
```

![Multiple](http://i.imgur.com/Ip4xy4s.jpg)

##### Disabled

Use the `disabled` option to make your switch active or inactive.

```js
var switchery = new Switchery(elem, { disabled: true });
```

Customize the default opacity of the disabled switch, using the `disabledOpacity` option.

```js
var switchery = new Switchery(elem, { disabled: true, disabledOpacity: 0.75 });
```

##### Colored

You can change the primary of the switch to fit your design perfectly:

```js
var switchery = new Switchery(elem, { color: '#41b7f1' });
```

![Colored](http://i.imgur.com/qO0Pzub.jpg)

Or the secondary color, which will change the switch shadow and default border:

```js
var switchery = new Switchery(elem, { secondaryColor: '#bbf0f0' });
```

Any other changes regarding colors you want to make, should take place in `switchery.css`.

##### Legacy browsers

If you are an adventurer and like to use legacy browsers, like IE8 and IE7, apply your favourite fix for rounded corners and box shadows and try a slightly different approach.

```js
var elems = document.querySelectorAll('.js-switch');

for (var i = 0; i < elems.length; i++) {
  var switchery = new Switchery(elems[i]);
}
```

## Credits

Big thanks to:

- [Veselin Todorov](https://github.com/vesln)

## Contact

If you like this component, share your appreciation by following me in [Twitter](https://twitter.com/abpetkov), [GitHub](https://github.com/abpetkov) or [Dribbble](http://dribbble.com/apetkov).

## License

The MIT License (MIT)

Copyright (c) 2013 Alexander Petkov

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.