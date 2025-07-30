
- Since ECMAScript 2015, JavaScript supports two different types of programs. 
	- Script behave in the old way: their bindings are defined in the global scope, and they have no way to directly reference other scripts. 
	- Modules get their own separate scope and support the `import` and `export` keywords, which aren't available in scripts, to declare their dependencies and interface. This module system is usually called `ES modules` 
- A modular program is composed of a number of such modules, wired together via their imports and exports. 
- They `export` keyword can be put in front of a function , class, or biding definition to indicate that that biding is part of the module's interface. This makes it possible for other modules to use that biding by importing it. 
