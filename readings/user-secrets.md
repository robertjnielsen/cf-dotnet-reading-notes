# User Secrets

## What Are User Secrets?

User Secrets in .NET applications are a way to securely store private data such as API keys, connection strings, client secrets, and more.

These are stored in a `secrets.json` file that is only accessible on the local machine via a `UserSecretsID`.

This file (and all the data it contains) is not uploaded to source control repositories, and is maintained only on the local machine.

## How To Use User Secrets

From within Visual Studio, right-click on your project file, and select `Manage User Secrets`.

This will open up the `secrets.json` file that you can then enter in your sensitive data in JSON format.

To access your user secrets data within your project you would add the following code to your `Startup.cs` file's constructor:

```cs
public IConfiguration Configuration { get; set; }

public Startup(IConfiguration configuration)
{
    var builder = new ConfigurationBuildere().AddEnvironmentVariables();

    builder.AddUserSecrets<Startup>();

    Configuration = builder.Build();
}
```

Our User Secrets file then gets added to our `builder` var which is going to instantiate our `Configuration` property declared on the first line.
