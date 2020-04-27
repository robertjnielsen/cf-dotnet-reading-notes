# View Components

## What Are View Components?

View components are similar to partial views, and may or may not contain logic.

_[Quote Source](https://mariusschulz.com/blog/view-components-in-asp-net-core-mvc)_
> View components include the same separation-of-concerns and testability benefits found between a controller and view. You can think of a view component as a mini-controller—it’s responsible for rendering a chunk rather than a whole response. You can use view components to solve any problem that you feel is too complex with a partial.

## Creating A View Component

To create a view component, we can:
- create a class that derives from the base `ViewComponent` class.
- create a class with the `[ViewComponent]` attribute.
- create a class with a name that ends with the `ViewComponent` suffix.

Any one or even a combination of the three will suffice.

Let's create a sample view componenet with the following code using all three methods:

```cs
[ViewComponent(Name = "Example")]
public class ExampleViewComponent : ViewComponent
{
    // Stuff and things here...
}
```

In the above code you can see that we created a ViewComponent class, ensured that it derived from the base class, and labeled it with an explicit name.