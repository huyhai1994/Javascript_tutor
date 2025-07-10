- Javascript provides a binary operator called `instanceof` to know whether an object was derived from a specific class.
```javascript


console.log([1] instanceof Array)
// -> true

```
- The operator will see through inherited types.
- The operator  can also be applied to standard constructors like `Array`
- Almost every object is an instance of `Object`.