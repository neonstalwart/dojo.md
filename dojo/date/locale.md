# dojo/date/locale

## Summary

This modules defines dojo/date/locale, localization methods for Date.
## Static Properties

### __FormatOptions


## Static Methods

### _getDayOfYear
gets the day of the year as represented by dateObject

### _getGregorianBundle


### _getWeekOfYear


### _getZone
Returns the zone (or offset) for the given date and options.  This
is broken out into a separate function so that it can be overridden
by timezone-aware code.


### _parseInfo


### addCustomFormats
Add a reference to a bundle containing localized custom formats to be
used by date/time formatting and parsing routines.


### format
Format a Date object as a String, using locale-specific settings.


### getNames
Used to get localized strings from dojo.cldr for day or month names.


### isWeekend
Determines if the date falls on a weekend, according to local custom.

### parse
Convert a properly formatted string to a primitive Date object,
using locale-specific settings.


### regexp
Builds the regular needed to parse a localized date

## Static Methods

### hasOwnProperty


### toString


