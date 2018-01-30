---
date: 2017-01-22T21:07:13+01:00
title: Unit Test
weight: 12
description: "What is a unit test and how does it fit into software development and the testing process."
---

## Introduction

Unit testing is the method of a software testing, by which source code of a program is divided into independent modules which are tested separately.

This method is most commonly used by software engineers in the process of developing. It is used to ensure if some separate module (piece of code) performs the right action. In object-oriented programming, we can consider methods or class as an independent unit. That's why it's crucial to identify independent modules of the source code, it should not reference any other module or piece. Considering that, we need to get rid of any dependencies while testing and isolate our module to test only its own functionality. 

Let's imagine this quick example. We have a program that reads two numbers from a console and says which one is bigger. 

As we can see on a diagram, user inputs two number, function receives them and generates result, depending on numbers we've set. 

If we wanted to apply Unit testing to this program, we would need to isolate our function. It means that we should avoid the user input, because we only want to assure that our function works well and not to test if user input works properly.

So, basically what we need to do is to simulate users input -- pass the function with pre-prepared values and to check if the function gives result that we expect. 

## Why do we need Unit testing?
Unit testing is needed by developers to verify if the piece of code they wrote works and works as it should. Unit testing could be a great contribution to the future, because if there would some code changes, it would save your time on testing and revealing possible issues. 

### Is it cost effective?
There are a lot of myths that grow near the Unit testing that it requires a lot of time and money, that developer should not make software tester's job and so on. But basically, if people who say so looked on it from a bit different perspective, it wouldn't seem like that at all. What if they considered Unit tests as a way to document that a developer checked that everything corresponds to the requirements? That doesn't sound that bad, right? Of course, it would take some time, but later code would be easier to edit or to add something new, because you won't have to worry about checking if everything okay if unit tests are done already.

## Automation

Unit testing is usually automated. It means that tests are executed automatically during every system build. To achieve this, we need to use some special tools, named test runners. There are different test runners in every language, for example JUnit (Java), Jasmine (JavaScript), unittest (Python) , Minitests( Ruby). They would help you to aggregate your tests, see tests run results, identify issues. 

Here's the example of a JUnit tests run results shown in Eclipse JUnit plugin.

Now let's see what is good and bad about Unit testing.

## Pros

1.  It is extremely fast. Tests are simple and small, that's why they're executed really fast. It is also automated. 
2.  It is precise. You can easily find the issue when something fails, because tests are independent and units are isolated.
3.  It is not expensive. It wouldn't require special people to write these tests. That is usually done by developers who wrote the code they're about to test.
4.  It's long lasting. It would help you to save time on regression later. 

## Cons

1.  It is time consuming. It requires developers to dedicate some extra time to write tests.
2.  It is not going to reveal all bugs. Even if you tested every independent unit of your application it would not guarantee that they would work fine together.
3.  It is hard to write realistic Unit tests. There are some situations in which it is hard to set up data for a unit to simulate it's work in the entire system. 

To sum up, unit testing is a great practice that would help you to control the quality of the product from the start, but you need to determine whether the results, you would get from it are worth time and resources you would have spent on it.