# LJ Code 201 - Day 3
**CODE REVIEW**
- Alert/Prompt windows is showing up before the page can render the content.
    - potential problem with the way Google is rendering the alerts/prompts
- Make sure if you are asking users for feedback that you tell them the feedback was properly received.
- cmd + d will multi select in atom
- make sure that in the future the code linter is installed correctly
- make sure to use proper spacing
- whenever you are doing any creative venture: “sometimes the best thing to do is to just write every crazy idea and then fix later.” (aka “write drunk, edit sober” “coding is recoding")
- if(answer1 === ‘yes’ || ‘y’)
    - will return a false positive because we don’t have an expression on the right side of the ||.
    - There is no evaluation operator on the right side and javascript will always read any expression that doesn’t use an evaluation operator.

**ARRAYS**
- Arrays are awesome!!
- Example Array:
  - var cars = ['Saab', 'Volvo', 'BMW'];
- - Arrays start with 0
- Access elements within an array by using the array order
    - cars[0] = Saab
- possible to reassign a position
    - cars[0] = ‘honda’;
    - new array looks like [‘honda’, ‘volvo’, ‘BMW’]
- Add to an array
    - by using blank space available in (i.e. cars[3] = ‘Toyota’;
        - new array looks like [‘honda’, ‘volvo’, ‘BMW’, ’Toyota']
    - .push is a method to add more data ( i.e. cars.push(‘Saab’); )
        - new array looks like [‘honda’, ‘volvo’, ‘BMW’, ’Toyota’, ’Saab']
- Arrays can contain any data type (i.e. string, boolean, number) and these data types can be mixed into the same array
    - best practice is to use similar data types in an array even though this is not required
- Arrays can be placed inside of other arrays
    - var vehicles = [cars, buses]
- to access an array inside of an array
    - vehicles[0] will access the cars array
    - vehicles[0][2] will access BMW because BMW is in the cars array and in the 2 position
- console.table(vehicles); will print in the console the arrays into a table so it’s easier to view.
    - this will be helpful to look at arrays that contain objects.

**JAVASCRIPT**
- Type coercion and weak typing
    - === vs ==
    - == (DON’T USE EVER) - this is a huge tell that you are noob
    - examples:
      - 2 == 2 (will be true)
      - 2 === 2 (will be true)
    - == tests across data types so that a (2 == ‘2’) will be “true"
      - == is a loose comparison and uses type coercion so that it will allow for false positives across.
    - === (USE THIS ALWAYS)
      - === is a strict comparison and requires that the data type is the same.
      - === prevents type coercion
