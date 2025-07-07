- In Javascript, *prototypes* could help Objects can be linked to other objects, to magically get all the properties that other object has. Plain old object created with {} notation are linked to an object call Object.prototype.
	``` javascript
	
	/*Object.prototype()*/  
	let empty = {}  
	console.log(empty.toString());  
	  
	console.log(Object.prototype.toString.call({}))
	```

- `toString()` is a method stored in `Object.prototype`, meaning that it is available in most object.

- When an object gets a request for a property that it doesn't have, its prototype will be searched for the property. If that doesn't have it, the `prototype's` prototype is searched, and so on until an object without prototype is reached (`Object.prototype` is such an object).
- `Object.getPrototypeof` returns the prototype of an object. Many object don't directly have `Object.prototype` as their prototype but instead have another object that provides a different set of default prototies. 
``` javascript
Array.prototype
Function.prototype

```

- use `Object.create` to create an object with a specific prototype. 

```javascript
	
	let protoRabbit = {  
    speak(line) {  
        console.log(`The ${this.type} rabbit says ${line}`)  
    }  
}  
let blackRabbit = Object.create(protoRabbit);  
blackRabbit.type = "black";  
blackRabbit.speak("heloo....")
```

=> The "proto" rabbit acts as a container for the properties shared by all rabbits. 