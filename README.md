### traceur-compiler
---
https://github.com/google/traceur-compiler
https://github.com/google/traceur-compiler/wiki/Adding-Transformation-Passes

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

/*
* @return {ParseTree}
* @private
*/
parsePropertyMethod_: function(){
  var start = this.getTreeStartLocation_();
  var name = this.nextToken_();
  this.eat_(TokenType.OPEN_PAREN);
  var formalParameterList = this.parseFormalParameterList_();
  this.eat_(TokenType.CLOSE_PAREN);
  var functionBody = this.parseFunctionBody_();
  return new PropertyMethodAssignment(this.getTreeLocation_(start), neme, formalParameterList, functionBody);
}

visitPropertyMethodAssignment: function(tree) {
  this.visitAny(tree.formalParameterList);
  this.visitAny(tree.functionBody);
},
```

```
```

