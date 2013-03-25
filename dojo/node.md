# Module: dojo/node

## Summary

This AMD plugin module allows native Node.js modules to be loaded by AMD modules using the Dojo
loader. Note that this plugin will not work with AMD loaders other than the Dojo loader.
## Examples

*       require(["dojo/node!fs"], function(fs){
        var fileData = fs.readFileSync("foo.txt", "utf-8");
      });


## Methods

### load
Standard AMD plugin interface. See https://github.com/amdjs/amdjs-api/wiki/Loader-Plugins
for information.

### normalize


