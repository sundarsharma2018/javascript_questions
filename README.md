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
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3
The number is 3


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



