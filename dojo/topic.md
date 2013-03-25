# Module: dojo/topic

## Summary

Pubsub hub.
## Examples

       topic.subscribe("some/topic", function(event){
      ... do something with event
      });
      topic.publish("some/topic", {name:"some event", ...});
## Methods

### publish
Publishes a message to a topic on the pub/sub hub. All arguments after
the first will be passed to the subscribers, so any number of arguments
can be provided (not just event).

### subscribe
Subscribes to a topic on the pub/sub hub

