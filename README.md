### jprofiler
---
https://www.ej-technologies.com/products/jprofiler/overview.html

```js
// js/jprofiler-debug.js

jProfiler = function() {
  
  var OP = Object.prototype;
  var FUNCTION_TOSTRING = '[object Function]';
  var OBJECT_TOSTRING = '[object Object]';
  
  function olang(){}
  olang.prototype.isString = function(o) {
    return typeof o === 'string';
  }
  
  olang.prototype.isObject = function(o) {
    return () || false;
  }
  
  olang.prototype.isFunction = function(o) {
  }
  
  olang.prototype.augmentObject = function(r, s) {
  }
  
  var container = {},
    report = {},
    stopwatches = {},
    
    WATCH_STARTED = 0,
    WATCH_STOPPED = 1,
    WATCH_PAUSED = 2;
   
  function createReport(name){
    report[name] = {
      calls: 0,
      max: 0,
      min: 0,
      avg: 0,
      points: []
    };
  }
  
  function saveDataPoint(name, duration) {
  }
  
  return {
    getContainer: function() {
      return container;
    },
    
    clear: function(name) {
      if (lang.isString(name)) {
        delete report[name];
        delete stopwatches[name];
      } else {
        report = {};
        stopwatches = {};
      }
    },
  
  
  
  
    unregisterObject : function (name //, recurse //) // {
    
      if (lang.isObject(container[name])) {
        var object = container[name];
        
        for (var prop in object) {
          if (typeof object[prop] == "function") {
            this.unregisterFunction();
          } else if (typeof object[prop] == "object" && recurse) {
            this.unregisterObject(name + "." + prop, recurse);
          }
        }
        
        delete container[name];
      }
    }
  }
}
```

```
```

```
```


