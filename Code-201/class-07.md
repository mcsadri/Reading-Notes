# Object-Oriented Programming, HTML Tables

## Domain Modeling

---

1. Explain why we need domain modeling. **A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.**

---

## HTML Table Basics

- A table allows you to quickly and easily look up values that indicate some kind of connection between different types of data.
- For tables to be effective on the web they some styling information with CSS, as well as good solid structure with HTML.
- HTML tables should be used for tabular data. They should not be used to lay out a webpage.
  - Layout tables reduce accessibility for visually impaired users.
  - Tables produce tag soup, meanging they are generally more complex and harder to write, maintain, and debug.
  - Tables are not automatically responsive.

``` html
    <table>
        <colgroup>
            <col>
            <col>
        </colgroup>
        <tr>
            <th></th>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
    </table>
```

---

1. Why should tables not be used for page layouts? **Poor accessiblity, tag soup, not automatically responsive**
2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.

- `<thead>` - semantic element to group table header rows
- `<tbody>` - semantic element to group table body rows
- `<tfoot>` - semantic element to group table footer rows

---

## JavaScript Object Basics

### Introducing Constructors

> - Used to define the "shape" of an object, aka the set of methods and properties it contains.
> - A constructor is just a function called using the `new` keyword.
> - When you call a constructor, it will:
>   - create a new object
>   - bind this to the new object, so you can refer to this in your constructor code
>   - run the code in the constructor
>   - return the new object.
> - Constructors, by convention, start with a capital letter and are named for the type of object they create.

``` javascript
function Person(name) {
  this.name = name;
  this.introduceSelf = function() {
    console.log(`Hi! I'm ${this.name}.`);
  }
}

const salva = new Person('Salva');
salva.name;
salva.introduceSelf();

const frankie = new Person('Frankie');
frankie.name;
frankie.introduceSelf();
```

> - Note that built in objects and APIs don't always create object instances automatically.
([from MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#youve_been_using_objects_all_along))

---

1. What is a constructor and what are some advantages to using it? **Constructors allow the developer to code the shape of an object a single time, and then use the `new` keyword to repeatedly create new objects of the same type with the constructor.**
2. How does the term `this` differ when used in an object literal versus when used in a constructor? **when you only have to create a single object literal, it's not so useful. But if you create more than one, this enables you to use the same method definition for every object you create.**

---

## Object Prototypes Using a Constructor

[A Beginner's Guide to JavaScript's Prototype](https://ui.dev/beginners-guide-to-javascript-prototype)

- Objects are key/value pairs
- The most common way to create an object is with curly braces {} and you add properties and methods to an object using dot notation
- **Functional Instantiation**: invoking a constructor function to construct a new object using the properties and logic encapsulated within the constructor function
- **Functional Instantiation with Shared Methods**: placement of shared methods in their object that can be then referenced by multiple other objects rather than repeating the same method in multiple objects.
- **Object.create**: allows you to create an object which will delegate to another object on failed lookups
  - Aka: object.create allows you to create an object and whenever there's a failed property lookup on that object, it can consult another object to see if that other object has the property.
- Functional Instantiation with Shared Methods and Object.create

### Prototype

- Every function in JavaScript has a prototype property that references an object
- **Prototypal Instantiation**: 
---

1. Explain prototypes and inheritance via an analogy from your previous work experience.  
   *NOTE: This is a very common front end developer interview question*

---
