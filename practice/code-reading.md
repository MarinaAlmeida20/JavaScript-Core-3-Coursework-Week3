# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.

Because the function don't recognize the number outside of the block of code(function), and the console.log don't know it has a number inside the function. All numbers declared inside a function belongs onl to the function and it can't be used outside of the function.

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
OUTPUT: ReferenceError: y is not defined
Because the 'y' was defined inside of a block of code, so it can't be access outside it.

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.
OUTPUT:
9
{ x: 10 }

9 => Because the first console.log on line 55, will console the value of the global variable declared on line 47.

{ x: 10 } => Because the console.log on line 65, will console the value of the global variable declared on line 57.
