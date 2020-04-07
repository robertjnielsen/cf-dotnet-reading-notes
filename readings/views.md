# Views

Views are how the server renders a "front-end" user interface. They are a combination of HTML and C# code, written with **_Razor Syntax_**. Views have a `.cshtml` file extension.

## View Layouts

Most web applications have a fairly consistent layout among most pages or views. Several elements, such as a header, footer, nav menu, and possibly even sidebar are the same on almost every page.

Instead of having to write out the code for these elements on each view or page, we can use layouts to handle that bit for us, and only modify the content that will be different on each view.

By convention, the default layout for an ASP.NET web app is called `_Layout.cshtml` and is located in the `Views/Shared/` directory.

To specify where the view dependent content will be rendered within a layout, use the `@RenderBody()` Razor syntax method call in the location you want the content to actually render.

To specify what layout a view should use, at the top of the View use the following:

```
@{
    Layout = "_Layout";
}
```

Notice in the above example we didn't have to specify a file path or file extension. ASP.NET Core automatically knows to look in the `Views/Shared/` directory, for a `.cshtml` file with the same name as the given layout name.
