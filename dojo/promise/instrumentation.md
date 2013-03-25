# Module: dojo/promise/instrumentation

## Summary

Initialize instrumentation for the Deferred class.
## Description

Initialize instrumentation for the Deferred class.
Done automatically by `dojo/Deferred` if the
`deferredInstrumentation` and `useDeferredInstrumentation`
config options are set.

Sets up `dojo/promise/tracer` to log to the console.

Sets up instrumentation of rejected deferreds so unhandled
errors are logged to the console.
