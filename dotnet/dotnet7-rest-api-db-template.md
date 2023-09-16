# .NET 7 REST API DB Template

This template is meant to help developers to build REST APIs:
 - with structured and layered solutions
 - using data persistance with Entitity Framework Core (SQL Server or SQL Database in the template)
 - using structured validation mecanisms
 - with configurable OpenAPI/Swagger exposition
 - with dynamic OpenAPI/Swagger documentation (including versioning)
 - with included API verioning (Url based)

The template also includes:
 - IoC/DI principles
 - generic exception management
 - default traces and logs
 - configurable integration with Application Insights
 - factorized mappings between layers
 - factorized DI
 - default test projects relying on the same IoC/DI principles than the actual solution (wich adds test integrity)

## Why?

One could wonder why in the minimalistic era we are living (Minimal APIs trend, etc), such a template could still be relevant.

The initial and natural use of such a template would be for complex and rich REST APIs. RESTFul APIs are not meant to contain business logic because of their nature and inherent definition (resource oriented, not business logic oriented).
This said, due to the "everything REST" trend, it is quite common to encounter (and even have to develop) business REST APIs.


