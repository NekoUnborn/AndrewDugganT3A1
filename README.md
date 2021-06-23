# AndrewDuggan_T3A1

## **Q1 - Provide an overview and description of a standard source control process for a large project.**

https://www.perforce.com/blog/vcs/what-source-control
https://www.atlassian.com/git/tutorials/comparing-workflows

Source (or version) control is the tracking of changes with software. This allows multiple developers to work on the same code without unintentionally overwriting each others work.

The centralised workflow uses a central repository that serves as a focus for all changes to the project. The first developer downloads a copy of the source files; Once they have been uploaded, any attempt to uploaded files with the incorrect version number will be checked for conflicts before being accepted.

## **Q2 - What are the most important aspects of quality software?**

<!-- CMP1043-2.2 - List discuss and demonstrate 6 software quality characteristics -->

### Functional Suitability

The functionality of software is from both the user and clients perspective, it includes making sure:

- the functions fulfil the requirements of the software,
- the software accurately depicts the wishes of the client
- the software can interact with all required systems.
- unauthorised use is prevented and it is resistant to the manipulation of the software or modification of the stored data.

### Efficiency


### Compatibility


### Usability

The usability of the software is the degree that the end-user can navigate the software in an efficient and effective way and have an overall sasfactory experience with the software

### Reliability

The reliability of the software can be defined by its resistance to changes in the host system, tolerance to software faults and its ability to maintain an active program in the event of a fault and to have the ability to recover its data in the event of a catastrophic failure.

### Security

### Maintainability

### Portability

<!-- ISO/IEC 25010 (2011) -->
<!-- https://www.springer.com/journal/11219 -->
<!-- Software Testing and Quality Assurance: Theory and Practice by Naik and Tripathy, 2008 -->
<!-- https://www2.cs.sfu.ca/~cameron/Teaching/473/quality_characteristics.html -->
<!-- https://en.wikipedia.org/wiki/Software_quality -->

## **Q3 - Outline a standard high level structure for a MERN stack application and explain the components.**

<!-- CMP1043-2.3 - Shows almost flawless understanding of the high level structure of the app -->

## **Q4 - A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project**

<!-- CMP1043-3.1 describes a range of skills and knowledge required by IT workers to complete a quality web development project -->

## **Q5 - With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges.**

<!-- CMP1043-3.2 describes a range of skills and knowledge used to complete a project. -->

## **Q6 - With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature.**

<!-- CMP1043-3.3 Evaluates effectiveness of knowledge and skills accurately, providing examples, and providing an insightful improvement on each skill -->

## **Q7 - Explain control flow, using an example from the JavaScript programming language.**

<!-- PRG1006-3.1 Provides a explanation of control flow in programming -->

## **Q8 - Explain type coercion, using examples from the JavaScript programming language.**

<!-- PRG1006-3.2 Provides a explanation of type coercion in programming -->

## **Q9 - Explain data types, using examples from the JavaScript programming language.**

<!-- PRG1006-3.3 Provides a thorough explanation of data types in programming -->

## **Q10 - Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language.**

<!-- PRG1006-5.1 Demonstrates an ability to manipulate arrays -->

## **Q11 - Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language.**

<!-- PRG1006-5.2 Demonstrates an ability to manipulate objects -->

## **Q12 - Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language.**

<!-- PRG1006-5.3 Demonstrates an ability to manipulate JSON -->

## **Q13 - For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes.**

<!-- PRG1006-4.1 Demonstrates an ability to recognise functions, ranges and classes -->

```javascript
// This class (Car) constructs the brand of the cars with this class
class Car {
  constructor(brand) {
    this.carname = brand;
  }

  // This function returns the name of the car brand from the instance, it is available to objects with this class
  present() {
    return "I have a " + this.carname;
  }
}

// This class (Model) is a subset of the Car class, it adds the model constructor
class Model extends Car {
  constructor(brand, mod) {
    // The super function allows Car.brand to be constructed from this class
    super(brand);

    // Allocates the second attribute to the model of this class instance
    this.model = mod;
  }

  // The show function returns the present function from the super class (Car) on the current instance and adds the model reference from this instance and is only available to objects of this class
  show() {
    return this.present() + ", it was made in " + this.model;
  }
}

// assigns the array to the makes variable
let makes = ["Ford", "Holden", "Toyota"];

// Creates an array containing a range between 1980 and 2019 and assigns it to the models variable
let models = Array.from(new Array(40), (x, i) => i + 1980);

// This function creates 40 random Cars through the Model class
function randomIntFromInterval(min, max) {
  // min and max included

  // This will return a random number (from 0-1), multiplies it by the max-min+1 to give a number between 0 max-min and finally adds the min. This will ultimately give a random number between min and max.
  return Math.floor(Math.random() * (max - min + 1) + min);
}

// Using this 'for' loop will create 40 cars as it uses the models array as a basis
for (model of models) {
  // randomIntFromInterval(0,makes.length-1) will give a value between 0 and 2 (as there are 3 elements in the makes array)

  // The make of the car wil be a random make from the makes array with a minimum index of 0 and a max of 2
  make = makes[randomIntFromInterval(0, makes.length - 1)];

  // The model of the car will be a random model between 1980 (index 0) and 1982 (index 2), I believe that this would be a bug and should be using the models array instead of the makes array for the random index
  model = models[randomIntFromInterval(0, makes.length - 1)];

  // This will actually create the new Model instance, this will only last for this loop and will be lost at the end of this loop
  mycar = new Model(make, model);

  //This will display the mycar object in the console
  console.log(mycar.show());
}
```
