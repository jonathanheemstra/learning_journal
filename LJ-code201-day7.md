# LJ Code 201 - Day 7
**Constructor Functions**
- Constructor functions are awesome and prevent rewriting code over and over. Hooray for D.R.Y.

**Working with Constructor Functions**
- create a constructor function by first creating a function
    - the name of the function should be capitalized:
        - Correct = `function Student() {}`
        - Incorrect = `function student() {}`
- for shared properties/methods
    - the syntax should look like:
        - `this.property = data;`
            - important to use ‘this’, =, and close with a  semi-colon
        - can be done for both properties and methods that are shared.
- for non-shared properties/methods
    - the properties and methods that need to be constructed are passed in via function variables/properties.
```
function Student(firstName, lastInitial, faveNumber) {
    this.course = '201d15'; //shared property
    this.firstName =  firstName; //unique property
    this.lastInitial =  lastInitial; //unique property
    this.faveNumber = faveNumber; //unique property
    this.isCodeNinja = true; //shared property
    this.introduction = function() { //shared method
        console.log('My name is ' + this.firstName + ' and my favorite number is ' + this.faveNumber);
  }
}
```
- To add data to the constructor function you need to create a new variable and assign values to the object properties
    - example:
        - `var jonny = new Student (‘Jonny’, ‘H’, 24);`
            - note: constructors don’t need “var name =“ but without it there isn’t an easy way to then access that newly constructed object.
        - `new Student (‘jonny’, ‘h’, 24);`
- Can take constructed objects and put them into an Array
    - example:
        - `var class = [jonny, marc, michael];`
            - note if all of these objects have been created they can be placed in an array.
- Can push newly created objects into a class (this is very common in constructor functions)
    - example

```
var class = [];

function Student(firstName, lastInitial, faveNumber) {
    this.course = '201d15'; //shared property
    this.firstName =  firstName; //unique property
    this.lastInitial =  lastInitial; //unique property
    this.faveNumber = faveNumber; //unique property
    this.isCodeNinja = true; //shared property
    this.introduction = function() { //shared method
        console.log('My name is ' + this.firstName + ' and my favorite number is ' + this.faveNumber);
  },
  class.push(this) //pushes newly created objects into array
}
```

- Accessing data from the class array can be done as usual.
    - example:
        - `class[0].firstName;`
- Editing/updating a constructed object by accessing the object needing to be updated via an array or by name (if not in an array) and then using dot notation.
    - `class[0].firstName = 'Jonny';`
- Adding to an existing object works the same as editing. Access the object needed to be updated and the using dot notation
    - `class[0].pokemon = 'Zubat';`
- Change something that changes all objects inside of a constructor function. AKA change the constructor.
    - `Student.prototype.course = '301d11';`
    - need to all the constructor function (aka Student)
    - prototype
        - prototypes can do some weird things in the console.
