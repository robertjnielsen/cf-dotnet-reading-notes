# Week One: Reading Notes Review

## My Chosen Topic To Review

I chose to review my [Unit Testing](unit-tests-and-documentation.md) notes for this weekly review session.

I chose this topic, because I feel that out of everything that we have covered so far, Unit Testing, and Test Driven Development will continue to have the most _coverage_ over all other topics moving forward.

## What Is Unit Testing?

Unit testing is the act of writing test methods, usually with some form of testing framework. In our case, we are using [xUnit](https://xunit.net/). These test methods are used to test a single **_unit_** of our code (usually a method, but a unit can be any singular item).

These tests are designed to be singular in nature, meaning that they do not rely upon any other methods or set-up outside of themselves.

Our tests are written in the form of **Arrange**, **Act** and **Assert**.

First we arrange the test:
- Declare any required variables, instances, etc.
- Essentially build out any resources we will need for our test.

Then we perform an act:
- We utilize what we're testing.
- We make method calls and grab values to be used in our assertion.

Finally, we assert something:
- We test that our actual outcome matches our expected outcome.
- This can be a comparison of equality, truthiness, or possibly many more options (though the first two are the most common).

Once our test has passed, we can move on to the next test.

## What Is Test Driven Development?

**Test Driven Development (or TDD)** is the act of performing tests during the course of writing your code, and not _after_ you've already written your code.

TDD is commonly accomplished by using the alogirithm for your code, and fleshing out the shell of a test based on that.

Then you can weeble-wobble back and forth between refactoring your code, and refactoring your test, ensuring that ultimately, your code works as expected, and is verified by passing tests!

This process is managed by: 
1. First knowing what you want your code to do, and how you think you're going to accomplish that.
2. Then writing out the most basic form of your test.
3. Refactoring either your test, or your code (or both) to make your test pass in the most basic, obvious form.
4. Repeating step 3 as many times as needed until your code is fully functional and accomplishes your goal, AND your test passes as expected.

## Why Unit Testing and TDD?

Testing your code ensures that your code will work. Though nothing is fullproof, this process will mitigate the overwhelming majority of possible bugs, errors, and edge cases that may occur when your compiled code runs.

Over time, this process actually saves time and effort. Shipping functional, tested code will require less time and effort refactoring and patching down the road as you move forward.
