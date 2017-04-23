# Base 26

## Prompt

Given a string of letters, calculate the value of the string as base 26.

## Methods

1. Hash of A-Z to 0-25
2. Walk through string and multiply it by the corresponding power

## Time Complexity
1. O(n) - n is length of string

## Space Complexity
1. O(1) - Math.pow is constant, using a single sum variable

## Notes

```javascript
function base26(str){
  var letterMap = {
    "A":0,
    "B":1,
    "C":2,
    "D":3,
    "E":4,
  }
  var sum = 0;
  var length = str.length;
  for (var i = 0; i < length; i++){
    console.log(letterMap[str[i]]*Math.pow(26,length-i-1));
    sum += letterMap[str[i]]*Math.pow(26,length-i-1);
  }
  return sum;
}

base26("BCB")
```