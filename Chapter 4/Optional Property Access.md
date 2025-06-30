## Usage
1. aren't sure whether a given value produces an object, but still want to read a property from it when it does
2. Aren't sure that a given property exits or when a variable might hold an undefined value.

```javascript
function city(object){
	return object.address?.city;
}
console.log("string".notAMethod?.());
console.log({}.arrayProp?.[0]);
```
