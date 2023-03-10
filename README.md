Q.1 -> whats output for this?
for (var val = 0; val < 3; val++) {
    console.log(val);
    setTimeout(function() {
        console.log(`The number is ${val}`);
    }, 1000);
}

o/p = 3,3,3


for (let i = 0; i < 3; i++) {
    console.log(i);
    setTimeout(function() {
        console.log(`The number is ${i}`);
    }, 1000);
}

o/p=0,1,2


====>>>>>
for (var val = 0; val < 3; val++) {
    console.log(val);
    setTimeout(function() {
        console.log(`The number is ${val}`);
    }, 1000);
}

o/p ===> 0
1
2
The number is 3
The number is 3
The number is 3.....infinite


<<<<<<<>>>>>>>=======================================>>>>>
-->closures aas pass ke enviroment ko yadd rkhta h. that is called closures
-->closures remembers its enviroment.
--> higher order function takes function and return function or both

function outer(){
    let a= 10;
    var b= 20;
    let inner = function() {
        console.log("inner", a,b);
    }
    return inner;
}
let result = outer();
result();

o/p ===>inner 10 20


function init() {
  var name = "Mozilla"; // name is a local variable created by init
  function displayName() {
    // displayName() is the inner function, that forms the closure
    console.log(name); // use variable declared in the parent function
  }
  displayName();
}
init();

o/p = Mozilla
=====================================================>>>>>>>

let test = base(2)
console.log(test(3)) //return 5
console.log(test(5)) // return 7 

o/p = 5
o/p =7

Answer;--->

 function base(x){
    let val = function(y){
        return x + y;
    }
}

let test = base(2)
console.log(test)===> it will return function 
  f (y) {
     return x * y;  //x have 2 value
}
console.log(test(3)) ===> 5  //y=3
console.log(test(5)) ===> 7  //y=5

------------------------------------------

function multipler(x){
    let fn= function(y){
        return x * y;
    }
    return fn; 
}
let multipler2 = multipler(2);
console.log(multipler2);
console.log(multipler2(3));




o/p == f (y) {
     return x * y;
}

o/p = 6;

<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>

Q3. What is the difference between innerHTML & innerText?
innerHTML – It will process an HTML tag if found in a string

innerText – It will not process an HTML tag if found in a string

Q4. What is an event bubbling in JavaScript?
Event bubbling is a way of event propagation in the HTML DOM API, when an event occurs in an element inside another element, and both elements have registered a handle for that event. With bubbling, the event is first captured and handled by the innermost element and then propagated to outer elements. The execution starts from that event and goes to its parent element. Then the execution passes to its parent element and so on till the body element.




<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>callback function

function modifyArray(arr, hello) {
    console.log(arr)
    hello();
}

var arr = [1, 2, 3, 4, 5];
modifyArray(arr, ()=>{console.log("hi")});

<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>
Q2: Given a string, reverse each word in the sentence


var string = "Welcome to this Javascript Guide!";

// Output becomes !ediuG tpircsavaJ siht ot emocleW
var reverseEntireSentence = reverseBySeparator(string, "");

// Output becomes emocleW ot siht tpircsavaJ !ediuG
var reverseEachWord = reverseBySeparator(reverseEntireSentence, " ");

function reverseBySeparator(string, separator) {
  return string.split(separator).reverse().join(separator);
}



<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>
Q3: How to check if an object is an array or not? Provide some code.


function greet(param) {
   if(typeof param === 'string') {
       console.log("Hi")
   }
   else {
         console.log("Hi1")
   }
 }
 
 
 var arrayList = [1 , 2, 3];
 
 greet(arrayList);


--->isArray() method is used to check if an object is an array. The Array. isArray() method returns true if an object is an array, otherwise returns false . Note: For an array, the typeof operator returns an object.


var arrayList = [1,2,3]
Array.isArray(arrayList);




<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>
Q4: How to empty an array in JavaScript?

method: 1====>

var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList = []; // Empty the array
console.log(anotherArrayList); // Output ['a', 'b', 'c', 'd', 'e', 'f']



method: 2====>

var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList.length = 0; // Empty the array by setting length to 0
console.log(anotherArrayList); // Output []

method: 3====>

var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList.splice(0, arrayList.length); // Empty the array by setting length to 0
console.log(anotherArrayList); // Output []


method: 4====>

while(arrayList.length) {
  arrayList.pop();
}


<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>
Q5: How would you check if a number is an integer or decimal?

function isInt(num) {
  return num % 1 === 0;
}

console.log(isInt(4)); // true
console.log(isInt(12.2)); // false
console.log(isInt(0.3)); // false

<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>
Q6: Implement enqueue and dequeue using only two stacks

Enqueue means to add an element, dequeue to remove an element.

// program to implement queue data structure

class Queue {
    constructor() {
        this.items = [];
    }
    
    // add element to the queue
    enqueue(element) {
        return this.items.push(element);
    }
    
    // remove element from the queue
    dequeue() {
        if(this.items.length > 0) {
            return this.items.shift();
        }
    }
    
    // view the last element
    peek() {
        return this.items[this.items.length - 1];
    }
    
    // check if the queue is empty
    isEmpty(){
       return this.items.length == 0;
    }
   
    // the size of the queue
    size(){
        return this.items.length;
    }
 
    // empty the queue
    clear(){
        this.items = [];
    }
}

let queue = new Queue();
queue.enqueue(1);
queue.enqueue(2);
queue.enqueue(4);
queue.enqueue(8);
console.log(queue.items);

queue.dequeue();
console.log(queue.items);

console.log(queue.peek());

console.log(queue.isEmpty());

console.log(queue.size());

queue.clear();
console.log(queue.items);


Q7: Stack

// program to implement stack data structure
class Stack {
    constructor() {
        this.items = [];
    }
    
    // add element to the stack
    add(element) {
        return this.items.push(element);
    }
    
    // remove element from the stack
    remove() {
        if(this.items.length > 0) {
            return this.items.pop();
        }
    }
    
    // view the last element
    peek() {
        return this.items[this.items.length - 1];
    }
    
    // check if the stack is empty
    isEmpty(){
       return this.items.length == 0;
    }
   
    // the size of the stack
    size(){
        return this.items.length;
    }
 
    // empty the stack
    clear(){
        this.items = [];
    }
}

let stack = new Stack();
stack.add(1);
stack.add(2);
stack.add(4);
stack.add(8);
console.log(stack.items);

stack.remove();
console.log(stack.items);

console.log(stack.peek());

console.log(stack.isEmpty());

console.log(stack.size());

stack.clear();
console.log(stack.items);


<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>Q7: Make this work

function duplicate(arr) {
  return arr.concat(arr);
}

duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]


<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>Q8: Write a "mul" function which will properly when invoked as below syntax

console.log(mul(2)(3)(4)); // output : 24
console.log(mul(4)(3)(4)); // output : 48


function mul (x) {
  return function (y) { // anonymous function
    return function (z) { // anonymous function
      return x * y * z;
    };
  };
}

<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>Q9: Write a function that would allow you to do this?
var addSix = createBase(6);
addSix(10); // returns 16
addSix(21); // returns 27


funcation createBase(x){
    let fn = funcation(y){
        return x+y;
    }
    retrun fn;
}

let addSix = createBase(6);
addSix(10);
addSix(21);


<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>Q10: FizzBuzz Challenge ---mid

Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and "fizzbuzz" at multiples of 3 and 5.

for (let i = 1; i <= 100; i++) {
  let f = i % 3 == 0,
    b = i % 5 == 0;
  console.log(f ? (b ? 'FizzBuzz' : 'Fizz') : b ? 'Buzz' : i);
}


<<<<<<<<<<>>>>>>>>>>=====================================================<<<<<<<<<>>>>>>>>>>>>>>>>
>Q11: Given two strings, return true if they are anagrams of one another  ----->Mid 
Problem
For example: Mary is an anagram of Army




