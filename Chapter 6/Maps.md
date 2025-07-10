A map (noun) is a data structure that associates values (the keys) with other values. 
```javascript



let ages = {
	Boris: 39,
	Liang: 22,
	Julia: 62
}
```

- Avoid using plain objects as maps because it's dangerous. Plain objects can have their keys collide with inherited properties from the prototype chain. For example, if a key named t`toString` is used, it might override the `toString` method from the Object prototype, leading to unexpected behavior.

- JavaScript have a class called `Map` which stores a mapping and allows any type of keys. 
```javascript


let ages = new Map();
ages.set("Boris", 39);
ages.set("Liang", 22);
ages.set("Julia", 62);


```

