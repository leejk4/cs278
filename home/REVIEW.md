# Code Review Process

## Overview

Every assignment will be code reviewed. These code reviews are designed to give you constructive feedback on how to improve from your peers. When you give feedback, you must be constructive and not demeaning or confrontational. 

## Review Requirements

You are responsible for assigning yourself 2 other students’ submissions to review.

Every student must review 2 other students’ assignments. __You must choose an assignment that has not already received 2 code reviews.__ You can check if an assignment has already received 2 reviews by looking for 2 “review/studentX/studentY” (see #4 below) branches. As soon as you choose 2 assignments to review, you should create and push your review branches to GitHub to ensure that you get those assignments “locked” to you. Otherwise, if two other people commit their review branches for that assignment before you, your review will not count towards your 2 review quota.

## Instructions

1.	Every assignment will have a “handin” or “merge” repo. You will need to clone this repo:

```bash
git clone <some repo url>
```

2.	For most assignments, your code will be submitted by creating and pushing to a submission/\<firstname\>\<lastname\> (e.g., submission/juleswhite) branch
3.	For code reviews, you will switch to the submission branch of the person that you are reviewing:

```bash
git checkout submission/<firstname><lastname>
```

4.	You will then need to create your own review branch from their submission branch that is named review/\<firstname\_of\_person\_being\_reviewed\>\<lastname\>/\<your\_firstname\>\<lastname\>. If Linus Torvalds was reviewing my code, he would do this:

```bash
git checkout submission/juleswhite
git checkout –b review/juleswhite/linustorvalds
```

5.	Create a REVIEW.md file that uses proper GitHub markup and follows the code review template here: https://github.com/cs4278-2015/home/blob/master/REVIEW_TEMPLATE.md
6.	Thoroughly review the code for your peer. 
7.	For each issue you identify, fix the issue in your review branch (or provide comments about how to fix it), commit the changes, push your branch to GitHub, and then submit a GitHub pull request with your change. You should commit fixes and create pull requests incrementally as you go so that the person being reviewed can see your thought process and doesn’t receive a single huge pull request. Linus might do something like this:

```bash
git add fix.js
git commit –m “This change fixes bug XYZ in QRS”
git push origin review/juleswhite/linustorvalds
```
Linus would then submit a GitHub pull request with the base branch being “submission/juleswhite” and a compare branch of “review/juleswhite/linustorvalds”

8.	Complete the REVIEW.md file per the template instructions
9.	Be prepared to present your review in class in a constructive, meaningful, and interesting way

## Due Dates

1.	All code reviews are due before class on the first Tuesday after the assignment due date

## Ground Rules

1.	Under no circumstances should your review be nasty, derogatory, demeaning, or otherwise insulting. 
2.	You should focus on “how to improve the code” not “why it isn’t any good.”
3.	You should NOT copy anything from another reviewer. Looking at someone else’s review of the submission you are reviewing is considered cheating. If you cut/paste or plagiarize part of another reviewer’s work, you will be referred to the honor council. Reviews should be your own original work.
4.	You should be thoughtful in your review. A review that simply provides a laundry list of minor formatting issues will not receive a high grade.

## Questions to Aid in Reviewing

1.	What are the assumptions that the developer made about what would and wouldn’t change? Are those assumptions accurate? Example: If I change the path that this is stored on the file system, will I have to change a lot of code? 
2.	Is there code duplication? If so, could the code be refactored to eliminate it?
3.	Do methods that form the interface points of APIs properly check their input and detect problems?
4.	How are exceptions handled? If a problem appears in a method, how far away will it be detected?
5.	Can you make random changes to their code, like swapping a false to true or changing branches of an if statement without breaking their tests? If so, what tests would they need to add to provide better coverage? 
6.	Are there obvious design patterns that could be used but aren’t?
