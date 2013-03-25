# Module: dojo/cache

## Summary

A getter and setter for storing the string content associated with the
module and url arguments.
## Description

If module is a string that contains slashes, then it is interpretted as a fully
resolved path (typically a result returned by require.toUrl), and url should not be
provided. This is the preferred signature. If module is a string that does not
contain slashes, then url must also be provided and module and url are used to
call `dojo.moduleUrl()` to generate a module URL. This signature is deprecated.
If value is specified, the cache value for the moduleUrl will be set to
that value. Otherwise, dojo.cache will fetch the moduleUrl and store it
in its internal cache and return that cached value for the URL. To clear
a cache value pass null for value. Since XMLHttpRequest (XHR) is used to fetch the
the URL contents, only modules on the same domain of the page can use this capability.
The build system can inline the cache values though, to allow for xdomain hosting.
## Examples

* To ask dojo.cache to fetch content and store it in the cache (the dojo["cache"] style
of call is used to avoid an issue with the build system erroneously trying to intern
this example. To get the build system to intern your dojo.cache calls, use the
"dojo.cache" style of call):

     //If template.html contains "<h1>Hello</h1>" that will be
     //the value for the text variable.
     var text = dojo["cache"]("my.module", "template.html");
* To ask dojo.cache to fetch content and store it in the cache, and sanitize the input
(the dojo["cache"] style of call is used to avoid an issue with the build system
erroneously trying to intern this example. To get the build system to intern your
dojo.cache calls, use the "dojo.cache" style of call):

     //If template.html contains "<html><body><h1>Hello</h1></body></html>", the
     //text variable will contain just "<h1>Hello</h1>".
     var text = dojo["cache"]("my.module", "template.html", {sanitize: true});
* Same example as previous, but demonstrates how an object can be passed in as
the first argument, then the value argument can then be the second argument.

     //If template.html contains "<html><body><h1>Hello</h1></body></html>", the
     //text variable will contain just "<h1>Hello</h1>".
     var text = dojo["cache"](new dojo._Url("my/module/template.html"), {sanitize: true});


