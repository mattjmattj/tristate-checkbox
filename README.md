# &lt;input is="tristate-checkbox"&gt;

> A checkbox that can be indeterminate

## Rationale

HTML5 provides a 3rd state to checkboxes, which is the "indeterminate" state.
This property can only be set using javascript, like in the example below:

```javascript
var cb = document.getElementById('whatever-checkbox');
cb.indeterminate = true;
```

Unfortunately, one cannot write the same thing in pure HTML, since "indeterminate"
is not an attribute. The following example will not work as expected:

```html
<input type="checkbox" indeterminate></input>
```

The goal of this custom element is to allow setting the "indeterminate" property
via an attribute.

## Demo

A (very ugly) live demo is available [here](http://mattjmattj.github.io/tristate-checkbox/)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install tristate-checkbox --save
```

Or [download as ZIP](https://github.com/mattjmattj/tristate-checkbox/archive/master.zip).

## Usage

1. Import Web Components' polyfill:

	```html
	<script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>
	```

2. Import Custom Element:

	```html
	<link rel="import" href="bower_components/tristate-checkbox/src/tristate-checkbox.html">
	```

3. Start using it!

	```html
	<input is="tristate-checkbox" indeterminate name="qux" id="baz"></input>
	```
	The custom element will do two things:
	
	1. add the attribute `type="checkbox"` if not already there
	2. set the `indeterminate` property according to the attribute value

## License

[MIT License](http://opensource.org/licenses/MIT)
