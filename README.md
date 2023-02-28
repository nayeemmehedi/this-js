## this in js  :palm_tree:

### Here are some common ways that this can be used  :do_not_litter: :


1. :smiling_imp: Global context: When used in the global context, this refers to the global object, which is window in web browsers or global in Node.js.



2. :smiling_imp: Object method: When a function is used as a method of an object, this refers to the object that the method is a property of. For example:



        const person = {
          name: "John",
          sayHello: function() {
            console.log("Hello, my name is " + this.name);
          }
        }

        person.sayHello(); // Outputs "Hello, my name is John"
        
        
        
 In this example, the sayHello() method is a property of the person object. When the method is called using person.sayHello(), this refers to the person object.
 
 
 
 3. :smiling_imp: Constructor function: When a function is used as a constructor function with the new keyword, this refers to the new object being created. For example:
 
 
         function Person(name) {
          this.name = name;
          this.sayHello = function() {
            console.log("Hello, my name is " + this.name);
          }
        }

        const john = new Person("John");
        john.sayHello(); // Outputs "Hello, my name is John"
        
        
        
   In this example, the Person function is used as a constructor to create a new Person object. When the sayHello() method is called using john.sayHello(), this refers to the john object that was created by the constructor function.
   
   
   
   
   4. :smiling_imp: Call and Apply methods: When a function is called using the call() or apply() method, this can be explicitly set to a specific object. For example:
   
   
   
   
           const person1 = {
              name: "John"
            }

            const person2 = {
              name: "Mary"
            }

            function sayHello() {
              console.log("Hello, my name is " + this.name);
            }

            sayHello.call(person1); // Outputs "Hello, my name is John"
            sayHello.apply(person2); // Outputs "Hello, my name is Mary"

          
          
          
 In this example, the sayHello() function is called using the call() and apply() methods, and this is explicitly set to person1 and person2, respectively.
 
 
 
 5. :smiling_imp: Arrow functions: In arrow functions, this is determined lexically, meaning that it takes on the value of this in the context where the arrow function was defined. For example:
 
 
 
 
             const person = {
              name: "John",
              sayHello: () => {
                console.log("Hello, my name is " + this.name);
              }
            }

            person.sayHello(); // Outputs "Hello, my name is undefined"
            
            
            
 In this example, the sayHello() method is an arrow function, so this takes on the value of this in the context where the arrow function was defined, which is the global object in this case. Therefore, this.name is undefined.

It's important to note that the value of this can be a bit tricky to understand in certain situations, especially when functions are nested or used in conjunction with event listeners. In these cases, it's important to pay close attention to the context in which the function is being executed to determine the value of `



 
 
