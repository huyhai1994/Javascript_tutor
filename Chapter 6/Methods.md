In JavaScript, methods are nothing more than properties that hold function values. 

``` javascript

function speak(line) {  
    console.log(`The ${this.type} rabbit says '${line}'`)  
}  // 
  
let whiteRabbit = {type: "white", speak};  
let hungryRabbit = {type: "hungry", speak};  
  
whiteRabbit.speak("Oh my fur and whiskers");  
hungryRabbit.speak("Got any carrots?");
```

Typically a method needs to do something with the object on which it was called. When a function is called as a method - looked up as a property an immediately called, as in `object.method()` - the biding called this in its body automatically points at the object on which it was called.
=> You can think of `this` as an extra parameter that is passed to the function in a different way than the regular parameters. 

