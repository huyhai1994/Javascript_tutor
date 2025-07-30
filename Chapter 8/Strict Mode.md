- Javascript can be made a little stricter by enabling `strict mode` 
	```javascript
	function canYouSpotTheProblem(){
		"use strict"
		for(count = 0; counter < 10; counter++){
			console.log("hi hi");	
		}
	}
canYouSpotTheProblem();
// -> ReferenceError: counter is not defined
```



- Code inside classes and modules is automatically strict. 
	If you're using CommonJS (NodeJS uses CommonJS modularization by default) there's no strict mode unless you include `"use strict"` in the file or execute node with the `--use_strict` flag. But in ECMAScript modules, strict mode is by default. You can enable it adding `"type": "module"` to package.json. [1](https://stackoverflow.com/questions/9031888/any-way-to-force-strict-mode-in-node)
- Putting "use strict" at the top of your program rarely hurts and might help you spot the problem.
- 