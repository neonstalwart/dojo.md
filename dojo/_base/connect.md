# Module: dojo/_base/connect

## Summary

This module defines the dojo.connect API.
This modules also provides keyboard event handling helpers.
This module exports an extension event for emulating Firefox's keypress handling.
However, this extension event exists primarily for backwards compatibility and
is not recommended. WebKit and IE uses an alternate keypress handling (only
firing for printable characters, to distinguish from keydown events), and most
consider the WebKit/IE behavior more desirable.
## Methods

### connect
`dojo.connect` is a deprecated event handling and delegation method in
Dojo. It allows one function to "listen in" on the execution of
any other, triggering the second whenever the first is called. Many
listeners may be attached to a function, and source functions may
be either regular function calls or DOM events.


### connectPublisher
Ensure that every time obj.event() is called, a message is published
on the topic. Returns a handle which can be passed to
dojo.disconnect() to disable subsequent automatic publication on
the topic.

### disconnect
Remove a link created by dojo.connect.

### isCopyKey
Checks an event for the copy key (meta on Mac, and ctrl anywhere else)

### publish
Invoke all listener method subscribed to topic.

### subscribe
Attach a listener to a named topic. The listener function is invoked whenever the
named topic is published (see: dojo.publish).
Returns a handle which is needed to unsubscribe this listener.

### unsubscribe
Remove a topic listener.

