---
date: 2017-01-29T21:07:13+01:00
title: Test Pyramid
type: index
weight: 10
---

## Introduction
> "No one in the brief history of computing has ever written a piece of perfect software. It's unlikely that you'll be the first." - Andy Hunt

Testing is an essential part of any kind of production, no matter what you're building. When it comes to software development, it's hard to imagine delivering a product to a customer without testing it first. You may be asking "Why so? Why don't developers just write code without errors and guarantee the quality by themselves? ". And the answer is pretty simple: it's hard to see your own errors. Especially when it comes to making something complex, you need that outside perspective to make sure that everything is alright. 

In the modern history there have been a lot of different examples of when people and businesses underestimated the process of testing and didn't put much effort in it, and as a result, paid the consequences. Some bugs can be extremely expensive. For example, in 2015 a software glitch caused a system wide [Bloomberg terminal crash](https://www.theguardian.com/business/2015/apr/17/uk-halts-bond-sale-bloomberg-terminals-crash-worldwide) that affected over than 300,000 traders globally. It's hard to even imagine how much money and nerves were burned during those hours of outage. 

But knowing that testing is important isn't enough. Testing is easy to get wrong and can be a massive distraction that at best eats away at your cash, but at worst can take up a lot of time and slow you down to a halt.

> “I'm not a great programmer; I'm just a good programmer with great habits.” - Kent Beck

While creating your testing strategy it's important to define an approach which makes sense for the product you're building, for your specific needs. Sorry, but there's no silver bullet, no one-size-fits all testing solution. There are however principles of testing that you can follow to help guide you, for example: *80% of defects are found in 20% of modules*, which means that you can identify some risky modules and put most of your effort in testing those. By following pricincipals like these we can harness the wisdom of our industry to devise a strategy which costs the least amount of energy while yielding the most amount of benefit.

Anther principle worth following is the approach of layered testing, of which the *Test Pyramid* is a great example. The test pyramid is a visual representation, a guide of sorts, to the best practices regarding what types of testing you should do together with how much effort, time, and money should be spent at each step. In short, the idea is that rather than trying to aim for 100% UI test coverage (for example), which would typically be flaky and slow to execute, to instead ration your efforts across various categories of testing in different layers of your product. Unit tests for example are known to be fast to execute and reliable, so they should typically form the foundation on which your testing should be built and most of your efforts spent on.

## Composition

The test pyramid consists layers on which different types of tests are performed. Basically, we break our system into granular units, and then put them together bit by bit and test at each stage. By taking this layered approach we can achieve a structured testing procedure which can fortunatenly be automated for the most part. In some products it may not be necessary to test on every layer, though caveat emptor, you do so at your own peril, as you'll be losing out on flexibility, extensibility and future saved time on bug fixing.


### Unit testing
The process of testing on the lowest level. The smallest parts of the code base should be identified, typically each individual function in the source code, and tested independently. Testing on this level is usually done by developers because they have a vision of how to divide the product source code into some independent logical parts, and also because it would take a lot of time for anyone else to review the code and understand it's structure. All the unit tests should be isolated and not depend on any other components or external systems.

### Component testing
Similar to unit testing, independent components should be identified and tested separately, but it is usually done by non-developers, and these components aren't pieces of source code, but the actual modules of the overall system.

### Integration testing
The main idea is to combine individual modules into groups of two or more components and check if they are working together properly. 

### System testing
Performed on the whole system to check if it corresponds to the expectations and requirements. Tests on this layer are typically user-based, meaning that they are tend to recreate user flows and reveal defects that are connected with actual user experience.

### End to End testing
For when your software depends on other systems or  uses third-party services, checking to see if everything works fine together. Think of it as "high level integration tests".

### Manual testing
At this level we test our entire system with all of services, sub-systems and other things which would be in the production version. On this level we want to verify that our product meets expectations by having humans actually use it and document the experience, taking note of any flaws encountered. 

