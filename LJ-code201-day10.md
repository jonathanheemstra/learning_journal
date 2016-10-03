# LJ Code 201 - Day 10

**Error Handling and Debugging**

- Part of fixing bugs is understanding the order of execution
    - remember the order of execution happens in the function calls
- Two important concepts
    - Context
        - deals with the environment the code is running in
    - Scope
        - where something can be accessed
- When we are writing code that is doing things: avoid
    - big pieces of code that are 40+, 60+ lines long
        - these are much much harder to figure out what is going on and debug and test
- Try to write code that breaks up larger chunks of code into smaller functions.
    - this allows you to better test pieces
    - you may identify that smaller functions do the same thing and can potentially remove repeated code that provides the same function.

**Scope**

- Scope is entirely determined by where the variable is declared.
- Global Scope
    - declared outside of any function (typically at the top of the code)
    - accessible anywhere including in any functions
- Limited Scope (function scope)
    - declared inside functions
    - only accessible within a function
- Why we might want to use limited scope
    - keeps the global space from being polluted
        - this is important for large projects
    - Ideally we should be declaring variables in a limited scope
        - prevents inadvertent naming errors causing problems on large projects
- Why we might want to use Global scope
    - when it’s not easy or efficient to use limited scope
- code smells
    - that immediate reaction you get when you view code.
        - is there large functions?
        - is there no indentation?
        - http://elijahmanor.com/javascript-smells/

**When working with Errors**

- ALWAYS read the error message and understand what the error is referencing
    - good practice to read through pages in chapter 10 (pg. 460-461)
- Writing smaller chunks of code will allow for better testing and debugging code
- Review Debugging Tips page (pg. 484)

**Wireframing**

- HTML when properly outlined should always look kinda like a document outline
- Steps in creating a web page
    1. Have a design concept and plan completely ready to go before you write the first line
        - wireframe showing all document dimensions
        - know where the images will go and how big they are
        - use placeholder images during the set up process
        - know where the text will go and use place holder
    2. Set up the project repo, scaffold the field, wire the files together
    3. ACP
    4. create a new branch
    5. build out all of the HTML
    6. ACP
    7. Create a new branch
    8. working top to bottom in the document, put the elements into place with CSS
    9. ACP
    10. Create a new branch
    11. Tweak responsiveness to the extent it is part of the design
    12. ACP
    13. Create a new branch
    14. Apply color, background, borders, other styling to the specifications of the design
    15. ACP
    16. Create a new branch
    17. Insert your content
    18. ACP
