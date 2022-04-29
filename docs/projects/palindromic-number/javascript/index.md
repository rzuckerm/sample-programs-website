---

title: Palindromic Number in Javascript
layout: default
date: 2022-04-28
last-modified: 2022-04-29

---

Welcome to the Palindromic Number in Javascript page! Here, you'll find the source code for this program as well as a description of how the program works.

## Current Solution

Note: The solution shown here is the current solution in the Sample Programs repository. Documentation below may be outdated.

{% raw %}

```Javascript
/*
Accept a number in command line
Print true,  if it is palindromic
Print false, if it is not palindromic
Print Usage: please input a non-negative integer, otherwise

Note: 
Empty text, blank string & long strings must fail
Minimum 2 digits must be present in the input
Tested using node
*/

const isPalindromic = (number) => {
    if(number <= 1){
    console.log("Usage: please input a number with at least two digits");
      process.exit(1);
    }  

    /*Count no. of digits, build reverse number*/ 
    let reverse_number = 0, no_of_digits = 0, temp = number;
    while(temp > 0){
      no_of_digits += 1;
      reverse_number = (reverse_number * 10) + (temp % 10);
      temp = Math.floor(temp / 10);
    }
    if (no_of_digits < 2){
      console.log("Usage: please input a number with at least two digits");
      process.exit(1);
    }  
    else
      if (reverse_number == number)
        return true;
      else 
        return false;

  };
  
  const input = process.argv[2];
  let number = Number(input)
  
  if (input !== '' && Number.isInteger(number) && number >= 0) {
    isPalindromic(input) ? console.log("true") : console.log("false");
  } else {
    console.log("Usage: please input a number with at least two digits")
  }

```

{% endraw %}

## How to Implement the Solution

No how to implement the solution available. Please consider contributing.

## How to Run the Solution

No how to run the solution available. Please consider contributing.