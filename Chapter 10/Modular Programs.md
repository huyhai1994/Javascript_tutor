
- A module is a piece of program that specifies which other pieces it relies on and which functionality it provides for other modules to use (its `interface`).
- They make part of the module available to the outside world and keep the rest private. 
- A good module system also requires modules to specify which code they use from other modules. These relations are called `dependencies`. If module A uses functionality from module B, it is said to depend on that module. 
- When the ways in which modules interact with each other are explicit, a system becomes more like LEGO, where pieces interact through well-defined connectors, and less like mud, where everything mixes with everything else. 
- 