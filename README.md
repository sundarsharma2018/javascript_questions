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
