# Database Seeing And Tag Helpers

## What Is Database Seeding?

Seeding is the process of filling a database with initial data.

## Ways To Seed Data With EF Core

#### Model Seed Data

In EF Core, seed data can be associated with an entity type as per the model configuration. At this point, the EF Core migrations can handle what operations need to be applied when updating the database.

#### Migration Customization

Manually adding the seed data to to a migration is another method of seeding a database with EF Core.

#### Custom Initialization Logic

The third method is to use `DbContext.SaveChanges()` before the main application logic executes.

## What Are Tag Helpers?

Tag Helpers enable server-side C# code to parcticipate in the creation and rendering of HTML elements within Razor pages and views.

### Tag Helpers Example

Look at the following example provided from [this](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/tag-helpers/intro?view=aspnetcore-2.1) Microsoft Docs page:

```
<label asp-for="Movie.Title"></label>
```

The previous example would render in the browser as such:

```
<label for="Movie_Title"></label>
```

This allows us to utilize our the model that we are passing to our Razor view, and write code that is easy to read and maintain from an MVC / OOP perspective, but also renders clean in the browser.

And that's all I have to say about that...
