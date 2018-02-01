---
date: 2017-02-01T21:07:13+01:00
title: Unit Test
weight: 12
description: "What is a unit test and how does it fit into software development and the testing process."
---

## Introduction

Unit testing is the method of software testing in which the source code of a program is divided into the smallest possible parts (units) which are then tested independently.

This method is most commonly used by software engineers during the process of product development. It is used to ensure that an isolated unit (piece of code) performs in the expected way. In object-oriented programming we can consider methods, functions, or sometimes even classes as independent units. It's crucial to identify independent units of the source code, as they should not reference any other units, modules or systems. To acoomplish this, it may be necessary to get rid of any dependencies while testing and isolate our unit so that it only tests its own functionality. 

Let's imagine this quick example: we have a program that reads two numbers from a console and says which one is bigger. 

If we wanted to apply unit testing to this program, we would need to isolate our function. It means that we should avoid the user input, because we only want to assure that our function works, not to test if user input works properly.

So, basically what we need to do is to simulate users input -- pass the function pre-prepared values and to check if the function returns the result that we expect. 

## Why do we need Unit testing?
Unit testing is needed by developers to verify that the piece of code they wrote works as expected. The biggest benefit it offers is that any future bugs encountered will be much easier to narrow down, as the unit tests will at the very least pin point the individual method that's causing trouble.

## Is it cost effective?
There are a lot of myths around unit testing that saying that it requires a lot of time and money, that developers should not be doing the QA/tester's job, and so on. However, if you look at it from a different perspective, then you'd see that it's not like that at all. What if you consider unit testing as a way to documenting that a developer has checked that everything corresponds to the requirements? That doesn't sound that bad, right? Sure it would take some time up front, but later, code would be much easier to refactor or to extend with new features because you won't have to worry about checking if everything is okay after each change - the unit tests are now paying you back for that effort you put in earlier.

## Automation

Unit testing is accomplished by writing specialized programs that import the functions to be tested, calls them, and then asserts (compares) that the expected output is returned. To achieve this, we need to use some special testing libraries (frameworks). There are different test libraries for every language, and they will help you to organize your tests, see tests run results, identify issues, and even isoloate depdencies and replace them with fakes/mocks.  

### Examples of test frameworks for some popular programming languages:
| Language   | Framework |
|------------|-----------|
| Java       | JUnit     |
| JavaScript | Jasmine   |
| Python     | unittest  |
| Ruby       | Minitests |


## Pros

1.  They are the fast. These tests are very quick to run because they are so simple, small and have no dependencies. 
2.  They are granular. You can easily find the issue when something fails because the tests are independent and the units are isolated.
3.  They are not expensive. You don't need to hire specialized staff, as unit tests are typically written by the same developers who are writing the code they want to test.
4.  They save time and increase confidence. Refactoring code and extending features is a way less risky operation if you know that you have a safety net of tests that will catch you if something were to go wrong. Also, you don't have to do repetative manual testing as these tests are programatically run.

## Cons

1.  They are time consuming in the short run. It requires that developers to dedicate some extra time to write tests which although in the long run typically saves you lots of time, will in the short term require extra work.
2.  They are not going to reveal all the bugs. Even if you tested every independent unit of your application it would not guarantee that they would work fine together.
3.  It is hard to write realistic unit tests. There are some situations in which it is hard to set up data for a unit to simulate it's work in the entire system. When isolating a unit from dependencies it can be quite easy to make a convoluted test which is mostly just testing the faked/mocked depdencency itself!