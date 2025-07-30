## The Document object model

- When you open a web page, your browser retrieves the page's HTML text and parses it. The browser builds up a model of the document's structure and uses this model to draw the page on the screen. 
-  The data structure the browser uses to represent the document follows this shape. ![[DOM example.png]]
- For each box, there is an object, which we can interact with to find out things such as what HTML tag it represents and which boxes and text it contains. This representation is called the `Document Object Model`, or DOM for short. 
- The global binding document is gives us access to these objects. 
- Since every HTML document has a head and a body, it also has head and body properties pointing at those elements. 
- 