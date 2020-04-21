# Razor Pages

Razor Pages are _similar_ to Razor Views, but with a couple major differences.

With the MVC architecture using Razor Views, a request is routed to a controller action, which then performs any business logic, and returns a response, usually in the form of a View.

With Razor Pages, a request is routed directly to a Razor Page, which then returns a response in the form of the Page itself, as well as any logic contained within the Page's PageModel.

## Example Directory Structures

A sample file structure could look like so with an MVC application:

```cs

-- Example.sln
  -- Example.csproj
  -- wwwroot
     -- Styles
       --> StyleSheet.css
     -- JavaScript
       --> Script.js
  -- Controllers
    --> HomeController.cs
    --> ThingController.cs
  -- ViewModels
    -- Examples
      --> Thing.cs
  -- Views
    -- Home
      --> Index.cshtml

```

A sample file structure with a Razor Pages app could look like so:

```cs

-- Example.sln
  -- Example.csproj
  -- wwwroot
     -- Styles
       --> StyleSheet.css
     -- JavaScript
       --> Script.js
  -- Pages
    -- Home
      --> Index.cshtml
        --> Index.cshtml.cs
    -- Things
      --> Things.cshtml
        --> Things.cshtml.cs

```