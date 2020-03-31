# MVC

## What Is MVC?

MVC is an architectural pattern known as **_Model, View, Controller_**. It allows seperation of concerns by diving our application components into three main groups or categories.

Using the MVC pattern, requests are routed to a **_controller_**, which can work with, query and perform actions on a **_model_**. The controller then chooses what **_view_** to display to the user, along with any model data required.

This seperation helps to scale the application as it grows or changes. If components of the application were written in a more inter-dependant manner, then you would have to change multiple items just to update one, etc and so on...

## What Is The Model?

The model is the business logic, state of the application, and hard data the application will be utilizing. For example, you could have a class called User that outlines the properties of an application user to be stored in a database. That class could be called the User model.

## What Is The View?

Views are how content are presented to the user. They make up the dynamic content, static layouts, etc. Views are the user information. In ASP.NET MVC, views are rendered with the Razor view engine that enables the embedding of .NET / C# code in HTML, and are stored with a file extension of `.cshtml`.

## What Is The Controller?

The controller is the traffic director of the MVC application. The controller handles requests, and determines what model to interact with, how to interact with it, how to handle user input and requests, and more.
