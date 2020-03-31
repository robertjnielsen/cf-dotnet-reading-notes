# Unit Tests And Documentation

## Unit Testing

### What Is Unit Testing?

Unit testing is the practice of testing your code, at the _unit_ level. What does that mean though?

Well in different languages, it could potentially mean a variety of things, but at its core it means a singular item. In the case of C#, we will be considering a singular method to be a unit. In this fashion, we can write tests that target a method and ensure it is working as intended.

### A Sample Test
_I'm pulling this example from [this Stackify article](https://stackify.com/unit-testing-basics-best-practices/) for ease and simplicity._

Assume you are creating a simple calculator method in C#:

```
public class Calculator
{
    public int Add(int x, int y)
    {
        return x + y;
    }
}
```

You want to test this **Add** method, and write up a simple unit test to handle this:

```
[TestClass]
public class CalculatorTests
{
    [TestMethod]
    public void Adding_9_And_2_Should_Return_11()
    {
        var calculator = new Calculator();
        int result = calculator.Add(9, 2);
        Assert.AreEqual(11, result);
    }
}
```
### Example Breakdown
Let's look at this a little closer.

The first thing our test class gets is the attribute `[TestClass]`, which tells Visual Studio's default test framework _**MSTest**_ that this class contains unit tests. As you can see, our method `Adding_9_And_2_Should_Return_11` also gets the attribute `[TestMethod]`, which as you can probably guess tells MSTest that that this is a test method.

Our method is named in a highly descriptive way, which tells us what our expected output should be given specific inputs.

Within our test method, we declare a new instance of our `Calculator` class.

We then invoke our calculator's `Add` method with our predefined inputs, and store the results in a variable declared as `result`.

Finally, we use MSTest's `Assert` class to determine if our `result` is equal to our expected output of **11**.

When run, the test will inform us of a pass or fail determined by the `Assert.AreEqual` method.

Congratulations, we have now _**MASTERED**_ unit testing!

_(We have NOT mastered unit testing, don't be so gullible...)_

## Documentation
Good documentation matters. We use a README file for this purpose. Its job is to inform our users, other devs, or really anyone else who is interested in our product the WHAT, HOW, WHY and more _about_ our product.

A good README should:  
1. Tell others WHAT our product is,
2. Show others what our product looks like in action,
3. Show them HOW to use it,
4. Fill in any other relevant details and information.

Good documentation IS your product. If a user cannot understand how to use your product from it's documentation, they won't use it. If a dev can't use your product without digging into your code to understand it, they probably (most likely) won't use it.

Your documentation should explain anything and everything neccessary for your product to be useful, while maintaining brevity (nobody needs to know how many cups of coffee you drank while writing a method).
