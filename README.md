# gkey #

A list of human-readable names for Browser-friendly gamepads. Currently only
supports generic/XBox-like controllers, but if you have the opportunity to test
with others then submit a pull request and I'll merge it in!

## Installation ##

``` bash
npm install gkey
```

## Usage ##

See [gp-controls](http://github.com/hughsk/gp-controls) for an example
implementation.

``` javascript
var generic = require('gkey/generic')
var xbox = require('gkey/xbox')

var gamepad = navigator.getGamepads()[0]

console.log(generic.buttons[0], gamepad.buttons[0]) // "<action 1>" 1
console.log(xbox.buttons[0], gamepad.buttons[0])    // "<a>" 1

console.log(generic.axes[0], gamepad.buttons[0])    // "<axis-left-x>" -0.75
console.log(xbox.axes[0], gamepad.buttons[0])       // "<axis-left-x>" -0.75
```
