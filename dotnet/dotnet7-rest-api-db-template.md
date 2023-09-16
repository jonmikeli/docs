# .NET 7 REST API DB Template

This template is meant to help developers to build REST APIs:
 - with structured and layered solutions
 - using data persistance with Entity Framework Core (SQL Server or SQL Database in the template)
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
[TODO]

## How to install it?
[TODO]

## How to use it?
[TODO]


## Template description
[TODO]