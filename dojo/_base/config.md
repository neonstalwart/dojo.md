# Module: dojo/_base/config

## Summary

This module defines the user configuration during bootstrap.
## Description

By defining user configuration as a module value, an entire configuration can be specified in a build,
thereby eliminating the need for sniffing and or explicitly setting in the global variable dojoConfig.
Also, when multiple instances of dojo exist in a single application, each will necessarily be located
at an unique absolute module identifier as given by the package configuration. Implementing configuration
as a module allows for specifying unique, per-instance configurations.
## Properties

### addOnLoad
Adds a callback via dojo/ready. Useful when Dojo is added after
the page loads and djConfig.afterOnLoad is true. Supports the same
arguments as dojo/ready. When using a function reference, use
`djConfig.addOnLoad = function(){};`. For object with function name use
`djConfig.addOnLoad = [myObject, "functionName"];` and for object with
function reference use
`djConfig.addOnLoad = [myObject, function(){}];`

### afterOnLoad


### baseUrl
The directory in which `dojo.js` is located. Under normal
conditions, Dojo auto-detects the correct location from which it
was loaded. You may need to manually configure `baseUrl` in cases
where you have renamed `dojo.js` or in which `<base>` tags confuse
some browsers (e.g. IE 6). The variable `dojo.baseUrl` is assigned
either the value of `djConfig.baseUrl` if one is provided or the
auto-detected root if not. Other modules are located relative to
this path. The path should end in a slash.

### callback
Defines a callback to be used when dependencies are defined before 
the loader has been loaded. When provided, they cause the loader to 
execute require(deps, callback) once it has finished loading. 
Should be used with deps.

### debugContainerId


### debugHeight


### defaultDuration
Default duration, in milliseconds, for wipe and fade animations within dijits.
Assigned to dijit.defaultDuration.

### deferredInstrumentation
Whether deferred instrumentation should be loaded or included
in builds.

### deps
Defines dependencies to be used before the loader has been loaded.
When provided, they cause the loader to execute require(deps, callback) 
once it has finished loading. Should be used with callback.

### dojoBlankHtmlUrl
Used by some modules to configure an empty iframe. Used by dojo/io/iframe and
dojo/back, and dijit/popup support in IE where an iframe is needed to make sure native
controls do not bleed through the popups. Normally this configuration variable
does not need to be set, except when using cross-domain/CDN Dojo builds.
Save dojo/resources/blank.html to your domain and set `djConfig.dojoBlankHtmlUrl`
to the path on your domain your copy of blank.html.

### extraLocale
No default value. Specifies additional locales whose
resources should also be loaded alongside the default locale when
calls to `dojo.requireLocalization()` are processed.

### ioPublish
Set this to true to enable publishing of topics for the different phases of
IO operations. Publishing is done via dojo/topic.publish(). See dojo/main.__IoPublish for a list
of topics that are published.

### isDebug
Defaults to `false`. If set to `true`, ensures that Dojo provides
extended debugging feedback via Firebug. If Firebug is not available
on your platform, setting `isDebug` to `true` will force Dojo to
pull in (and display) the version of Firebug Lite which is
integrated into the Dojo distribution, thereby always providing a
debugging/logging console when `isDebug` is enabled. Note that
Firebug's `console.*` methods are ALWAYS defined by Dojo. If
`isDebug` is false and you are on a platform without Firebug, these
methods will be defined as no-ops.

### locale
The locale to assume for loading localized resources in this page,
specified according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt).
Must be specified entirely in lowercase, e.g. `en-us` and `zh-cn`.
See the documentation for `dojo.i18n` and `dojo.requireLocalization`
for details on loading localized resources. If no locale is specified,
Dojo assumes the locale of the user agent, according to `navigator.userLanguage`
or `navigator.language` properties.

### modulePaths
A map of module names to paths relative to `dojo.baseUrl`. The
key/value pairs correspond directly to the arguments which
`dojo.registerModulePath` accepts. Specifying
`djConfig.modulePaths = { "foo": "../../bar" }` is the equivalent
of calling `dojo.registerModulePath("foo", "../../bar");`. Multiple
modules may be configured via `djConfig.modulePaths`.

### parseOnLoad
Run the parser after the page is loaded

### require
An array of module names to be loaded immediately after dojo.js has been included
in a page.

### transparentColor
Array containing the r, g, b components used as transparent color in dojo.Color;
if undefined, [255,255,255] (white) will be used.

### useCustomLogger
If set to a value that evaluates to true such as a string or array and
isDebug is true and Firebug is not available or running, then it bypasses
the creation of Firebug Lite allowing you to define your own console object.

### useDeferredInstrumentation
Whether the deferred instrumentation should be used.

* `"report-rejections"`: report each rejection as it occurs.
* `true` or `1` or `"report-unhandled-rejections"`: wait 1 second
in an attempt to detect unhandled rejections.

