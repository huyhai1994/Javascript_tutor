-  A classes defines the shape of a type of object - what methods and properties it has. Such an object is called an `instance` of the class.
- Prototypes are useful for defining properties for which all instances of a class share the same value. Properties that differ per instance need to be be stored directly in the objects themselves.
- Javascript's class notation makes it easier to define this type of function, along with a prototype object.
```javascript

class Rabbit{
	constructor(type){
		this.type = type;
	}
	speak(line){
			console.log(`The ${this.type} rabbit says ${line}`)
	}
}
```
- Any number of methods may be written inside the declaration's braces. 
- This function cannot be called like a normal function. Constructors, in JavaScript, are called by putting the keyword `new` in front of them. 
	=>  creating a fresh instance object whose prototype is the object from the function's prototype property, they runs the function with this bound to the `new` object, and finally returns the object. 
	```javascript
		let killerRabbit = new Rabbit ("killer")
	```
- The actual prototype of a constructor is `Funtion.prototype` since constructors are functions. The constructor function's prototype property holds the prototype used for instances created through it. 


```javascript

console.log(Object.getPrototypeOf(Rabbit) === Function.prototype)

// -> true

console.log(Object.getPrototypeOf(killerRabbit)===
Rabbit.prototype)
// -> true

```