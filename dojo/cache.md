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
