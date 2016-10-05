# LJ Code 201 - Day 13
- Local storage is awesome. I am already thinking of ways that I could use this. In particular I think it would super helpful when creating an application like a game where a score needs to be saved or added.
- The semantics for setting up the local storage call seem a big tough right now but I am hoping that after practicing with them for a a while I will be able to get them down.

**Final Projects**
- Individual and Group Project
    - Keep list of all the things you do for the project
        - Overall contributions
        - Code contributions
        - Collaboration contributions
- Setting Projects and Teams
    - project pitches on Thursday and Friday
    - Teams will be set as a balanced team and handed out on Friday

**UI/UX discussion**
- Learning good things in UI/UX is a blend of learning what to do and what not to do.
- Sometimes the best way to find the best UI/UX is to look at other websites and see what other websites do.
- Run/test changes with 3rd party people.

**Persistence in Local Storage**
- Why do we bother studying Local Storage
    - local storage is about getting feet wet in the concept of persistence
    - persistence
        - how we share information
        - keep information over time
    - persistence types
        - volatile = temporary (aka RAM)
        - non-volatile = not temporary (aka Hard Drive)
    - different types of persistence
        - no persistence
        - sessions storage
            - lives as long as the browser is open (aka volatile)
            - data cleared when the session ends
        - local storage
            - lives beyond the browser being open. (aka non-volatile)
            - data cleared when user clears it.
        - remote storage
            - lives in remote database (aka non-volatile)
- Why use it
    - share data between multi pages on a website
    - preserve data between sessions
- What info we should store
    - unique data specific to a given user.
        - NOTE: local store can’t store methods or functions
    - when you make objects from a constructor function you loose the inheritance link to the constructor
- When to store data
    - best time to capture data is when the data changes.
- When to retrieve data
    - best time is on page load/page refresh
- Local storage stores everything as a string
    - first thing we need to do is convert data into a string before pushing data into local storage
        - stringify
    - when retrieving data the data will need to be converted back into a data structure.
        - parse
- Create and Retrieve data from local storage

```
var students = ['Kenneth', true, 34, 'Danny-Man', true, 66, 'Sugey', true, 92];
> students
>> ["Kenneth", true, 34, "Danny-Man", true, 66, "Sugey", true, 92]

var studentsStringified = JSON.stringify(students);
> studentsStringified
>> "["Kenneth",true,34,"Danny-Man",true,66,"Sugey",true,92]"

localStorage.setItem('demo',studentsStringified)
>> (in console) >> application >> key/value pairs

var studentsRetrieved = localStorage.getItem('demo')
> studentsRetrieved
>> "["Kenneth",true,34,"Danny-Man",true,66,"Sugey",true,92]"

var studentsParsed = JSON.parse(studentsRetrieved)
> studentsParsed
>> ["Kenneth", true, 34, "Danny-Man", true, 66, "Sugey", true, 92]

> students
>> ['Kenneth', true, 34, 'Danny-Man', true, 66, 'Sugey', true, 92]
 ```

 - When loading a page need to check for local storage

```
if (local storage exists) {
   retrieve and parse Local storage
   assign that to objects
   carry on
} else {
   create objects
   carry on
}
```

- Clear local storage

```
localStorage.clear();
```
