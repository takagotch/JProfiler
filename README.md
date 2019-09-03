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
  
  }
}
```

```
```

```
```


