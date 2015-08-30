# Assignment 3

## Overview

For this assignment, you will be substantially improving the test coverage of the Dropbox application and the feature that you added to it. You must use the Mocha Javascript testing framework and Should JS assertions library to add new tests for the application. You are expected to substantially improve the test coverage and robustness. Adding just a few tests is unlikely to cut it.
Grading Standard

We will be using a “whammy” or “chaos monkey” to grade your application. These automated tools will randomly change parts of your code to produce syntactically correct Javascript. We will run multiple iterations of these tools against your codebase to make changes. You will be scored based on the percentage of these changes that cause one of your tests to fail. Ideally, all of these changes will cause at least one of your tests to fail, yielding a perfect score. Your tests must provide high coverage to perform well against the whammy.

Here are some examples of things the “whammy” might change:

```javascript
if(!foo) → if(foo)

if(a < 3 && b > 2) → if(a<= 3 && b > 2)

var a = 4 → var a = 4.1

function foo(a,b) → function foo(b,a)
```

Be prepared.

## Part 1: Instructions

1.	Clone the repo that you will be merging into https://github.com/cs4278-2015/assignment3-handin
2.	Create a branch titled submission/\<firstname\>\<lastname\> (e.g., submission/juleswhite) 
3.	Add as many Mocha tests as you need to feel like your code is ready for the whammy
4.	Commit your code to your submission branch
5.	Push your branch to GitHub (double check that it shows up on GitHub)


## Part 2: Instructions
1.	Complete code reviews for 2 of your peers using the process described in the home GitHub repo

## Part 3: Instructions
1.	Merge or reject (with detailed comments) all pull requests from your reviews

## Grading Standard

- 30% - Part 1 / percentage of whammy changes that cause one of your tests to fail
- 20% - Part 1 / quality of your tests
- 40% - Part 2 / code review quality of others’ solutions
- 10% - Part 3 / prompt and thoughtful response to pull requests

## Due Dates

1.	Part 1 with your code is due at 11:59pm on 9/20
2.	Part 2 with your code reviews of other peoples’ solutions is due at 10:00am on 9/22 and will be presented in class
3.  Part 3 is due before class on 9/24


