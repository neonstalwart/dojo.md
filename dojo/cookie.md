# Module: dojo/cookie

## Summary

Get or set a cookie.
## Description

If one argument is passed, returns the value of the cookie
For two or more arguments, acts as a setter.
## Examples

* set a cookie with the JSON-serialized contents of an object which
will expire 5 days from now:

      require(["dojo/cookie", "dojo/json"], function(cookie, json){
        cookie("configObj", json.stringify(config, {expires: 5 }));
      });


* de-serialize a cookie back into a JavaScript object:

      require(["dojo/cookie", "dojo/json"], function(cookie, json){
        config = json.parse(cookie("configObj"));
      });


* delete a cookie:

      require(["dojo/cookie"], function(cookie){
        cookie("configObj", null, {expires: -1});
      });


## Methods

### isSupported
Use to determine if the current browser supports cookies or not.

Returns true if user allows cookies.
Returns false if user doesn't allow cookies.

