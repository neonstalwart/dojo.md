# Module: dojo/currency

## Summary

localized formatting and parsing routines for currencies
## Description

extends dojo.number to provide culturally-appropriate formatting of values
in various world currencies, including use of a currency symbol.  The currencies are specified
by a three-letter international symbol in all uppercase, and support for the currencies is
provided by the data in `dojo.cldr`.  The scripts generating dojo.cldr specify which
currency support is included.  A fixed number of decimal places is determined based
on the currency type and is not determined by the 'pattern' argument.  The fractional
portion is optional, by default, and variable length decimals are not supported.
## Properties

### __FormatOptions


### __ParseOptions


## Methods

### _mixInDefaults


### format
Format a Number as a currency, using locale-specific settings


### parse


### regexp


# Constructor

## Methods

### hasOwnProperty


### toString


