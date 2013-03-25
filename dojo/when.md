# dojo/when

## Summary

Transparently applies callbacks to values and/or promises.
## Description

Accepts promises but also transparently handles non-promises. If no
callbacks are provided returns a promise, regardless of the initial
value. Foreign promises are converted.

If callbacks are provided and the initial value is not a promise,
the callback is executed immediately with no error handling. Returns
a promise if the initial value is a promise, or the result of the
callback otherwise.
