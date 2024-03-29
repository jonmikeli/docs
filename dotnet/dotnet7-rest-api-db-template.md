# .NET 7 REST API DB Template

This template is meant to help developers to build REST APIs:
 - with structured and layered solutions
 - using data persistence with Entity Framework Core (SQL Server or SQL Database in the template)
 - using structured validation mechanisms
 - with configurable OpenAPI/Swagger exposition
 - with dynamic OpenAPI/Swagger documentation (including versioning)
 - with included API versioning (Url based)

The template also includes:
 - IoC/DI principles
 - generic exception management
 - default traces and logs
 - configurable integration with Application Insights
 - factorized mappings between layers
 - factorized DI
 - default test projects relying on the same IoC/DI principles than the actual solution (which adds test integrity)

## Why?

One could wonder why in the minimalistic era we are living (Minimal APIs trend, etc), such a template could still be relevant.

### REST "Business" APIS?

The initial and natural use of such a template would be for complex and rich REST APIs. RESTFul APIs are not meant to contain business logic because of their nature and inherent definition (resource oriented, not business logic oriented).
This said, due to the "everything REST" trend, it is quite common to encounter (and even have to develop) business REST APIs.

### "Simple" APIs vs Complex APIs

With this in mind, rich and business APIs might start "simple" but, quite soon, they grow and end up needing some structure and segregation of concerns.
This template anticipates that and, even though it might seem a bit overkill for an initial and simple API, it will help developers to keep their code clean and structured.

### A concentrate of "how tos"

Technology evolves fast, very fast. At the same time, developers come from very different paths, some of them not giving time, importance or focus enough to specific topics. Saying that all the needed concepts, principles and patterns are understood, there is still a need to know how to use a given technology stack to implement them. This template tries to help with that.
Of course, the template integrates specific choices when it comes to some practices or ways to solve problems. This is not meant to be the only way to do things, but it is a way that works and that can be used as a starting point.

## Where to find it?

The extension might be found:
 - in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/?WT.mc_id=AZ-MVP-5004280) (Visual Studio version)
 - in NuGet.org repository (.NET CLI version)

> NOTE
>
> Visual Studio is able now to view and use extensions packaged as NuGet packages. Installing the VSIX (Visual Studio Extension native format) is not necessary if you already have the NUGet package installed.
> The NuGet package might be used either through Visual Studio or .NET CLI.

## How to install it?

### Visual Studio

The extension might be installed from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/?WT.mc_id=AZ-MVP-5004280).
If the VSIX is downloaded to the local machine, you only need to double-click on it and it triggers the installation process.

The extension can also be installed from the Extensions menu in Visual Studio.

### .NET CLI

The extension might be installed from the [NuGet.org repository](https://www.nuget.org/packages) using the following command:

```bash
dotnet new -i <package name>
```

## How to use it?

### Visual Studio

The use of the template is quite straightforward.
Once the extension is installed, it can be found in the list of available templates when creating a new project.
The project creation assistant will guide you through the process asking the required inputs.
 
### .NET CLI

Once the extension is installed, it can be found in the list of available templates when creating a new project.
The solution creation command line requires some parameters.
To know which parameters are needed, you can use the following command:

```bash
dotnet new <template name> --help
```

Solution creation command:

```bash
dotnet new <template name> -n <solution name>
```


## Template description
[TODO]