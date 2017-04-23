# Fibonacci number

## Prompt

1. Given the nth element, return the value of that element based on the Fibonacci sequence.


`0 1 1 2 3 5 8 13 ...`

## Methods

Recursion

## Time Complexity

exponential time


```a**n == a**(n-1) + a**(n-2)```


Divide through by a(n-2):


```a**2 == a + 1```


```a == (1+sqrt(5))/2```


## Space Complexity

`(# of stack frames)*(space per stack frame)`. 
`n stack frames f(n), f(n-1), f(n-2), ..., f(1)` 
`O(1) space per stack frame (to store the argument n)`
`We only care about how many stack frames there are at a time. Once a function returns, it's no longer using stack space.`

## Notes
```javascript
function fib(n){
  if(n<1){return "n must be positive integer greater than 0";}
  if(n===1){return 0;}
  if(n===2){return 1;}
  return fib(n-1)+fib(n-2);
}

fib(8)
```