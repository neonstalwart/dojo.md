# Module: dijit/BackgroundIframe

## Summary

For IE/FF z-index schenanigans. id attribute is required.

## Description

new dijit.BackgroundIframe(node).

Makes a background iframe as a child of node, that fills
area (and position) of node
# Constructor

## Methods

### destroy
destroy the iframe

### resize
Resize the iframe so it's the same size as node.
Needed on IE6 and IE/quirks because height:100% doesn't work right.

