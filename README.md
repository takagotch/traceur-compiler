### traceur-compiler
---
https://github.com/google/traceur-compiler

```js
class Greeter {
  constructor(message) {
    this.message = message;
  }
  
  greet() {
    var element = document.querySelector('#message');
    element.innerHTML = this.message;
  }
};
var greeter = new Greeter('Hello');
greeter.greet();

import './Greeter.js';

window.System = new traceur.runtime.BrowserTraceurLoader();
System.import('./Greeter.js');
```

```js
var object = {
  prop: 42,
  method() {
    return this.prop;
  }
};

var object = traceur.runtime.markMethod({
  prop: 42,
  method: function(){
    return this.porp;
  }
}, ['method']);
```

```
```

