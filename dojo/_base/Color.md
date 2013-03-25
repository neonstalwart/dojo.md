# Module: dojo/_base/Color

## Summary

Takes a named string, hex string, array of rgb or rgba values,
an object with r, g, b, and a properties, or another `Color` object
and creates a new Color instance to work from.

## Examples

* Work with a Color instance:

     var c = new Color();
     c.setColor([0,0,0]); // black
     var hex = c.toHex(); // #000000


* Work with a node's color:

     var color = dojo.style("someNode", "backgroundColor");
     var n = new Color(color);
     // adjust the color some
     n.r *= .5;
     console.log(n.toString()); // rgb(128, 255, 255);


## Properties

### named
Dictionary list of all CSS named colors, by name. Values are 3-item arrays with corresponding RG and B values.

## Methods

### blendColors
Blend colors end and start with weight from 0 to 1, 0.5 being a 50/50 blend,
can reuse a previously allocated Color object for the result

### fromArray
Builds a `Color` from a 3 or 4 element array, mapping each
element in sequence to the rgb(a) values of the color.

### fromHex
Converts a hex string with a '#' prefix to a color object.
Supports 12-bit #rgb shorthand. Optionally accepts a
`Color` object to update with the parsed value.


### fromRgb
get rgb(a) array from css-style color declarations

### fromString
Parses `str` for a color value. Accepts hex, rgb, and rgba
style color values.

### makeGrey
creates a greyscale color with an optional alpha

# Constructor

## Properties

### a


### b


### g


### r


## Methods

### sanitize
makes sure that the object has correct attributes

### setColor
Takes a named string, hex string, array of rgb or rgba values,
an object with r, g, b, and a properties, or another `Color` object
and sets this color instance to that value.


### toCss
Returns a css color string in rgb(a) representation

### toHex
Returns a CSS color string in hexadecimal representation

### toRgb
Returns 3 component array of rgb values

### toRgba
Returns a 4 component array of rgba values from the color
represented by this object.

