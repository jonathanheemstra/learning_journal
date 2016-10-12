# LJ Code 201 - Day 15
- Git team workflow is so much different than working on a project as an individual. It's going to take a lot more practice to get the flow down correctly.
- Getting the process is going to take some work.


**Git workflow for teams**

- Team workflow is different than the pair programming model
    - pair programing workflow (aka open source workflow)
        - fork copy of person 1 repo
        - clone forked copy of person 1 repo to local
        - ACP back to forked repo on git hub
        - pull request back to person 1 master repo
        - person 1 pull updated/merged master repo back to their local
    - team workflow
        - team members set as collaborators on a repo
            - All team members have equal rights to merge to master
            - no need to fork repo
        - team members clone repo to local
        - team members can create branches
            - other team members can access and pull a branch down
        - Team members all can push, pull, and merge to master repo
    - how to prevent merge conflicts
        - don’t do simultaneous work on the same branch
        - frequent and regular pulling
            - git pull origin master
    - Always do you work on branches! never commit to master.
- https://github.com/codefellows/seattle_201d15/blob/master/class-14-js_inheritance-css_animations/git-team-workflow.md

**Javascript topics**

- ES6 is the new standard
- JavaScript is changing so quickly it’s important to keep learning how to use the newest and greatest tools
- Learn String Methods and Array Methods.
- IFFE = immediately invoked function expressions
    - a tool to manage the order in which JS is executed
    - will run the function as soon as the interpreter gets to the code
        -  example:
        - create a variable and a nameless function wrap the function in parens and then following the ending ‘}’ you call the function with “( )”.
```
var x = (function() {
  return Y;
}());
```
    - common use = functions that should run on page load
- D.R.Y.
    - cook things down into the smallest pieces possible. Especially if you do things over and over again.
```function createElement (content, parent, child) {
}
```

- Pass by reference vs Pass by value
    - Pass by value = If we have a var that contains a primitive value (number, string, boolean) that var can be assigned in to another variable but these var will maintain their uniqueness if one or the other is later changed.
```
var a = 123;
var b = a;
b >> 123
var a = 456;
a >> 456
b >> 123
```
```
var a = [1,2,3];
var b = a;
b >> [1,2,3]
a[3] = ‘pbr’;
a >> [1,2,3,”pbr”]
b >> [1,2,3,”pbr”]
c = [a[0], a[1]]
c >> [1,2]
a[0] = ‘jojo’
c >> [1,2]
a >> [‘jojo’, 2,3,’pbr’]
```
    - Pass by reference = if you pass a structure (i.e. not a primitive value) this will create a “pointer” that always points the same spot in the memory so that if one changes the other will change.
```
var a = [1,2,3];
var b = a;
b >> [1,2,3]
a[3] = ‘pbr’;
a >> [1,2,3,”pbr”]
b >> [1,2,3,”pbr”]
```
