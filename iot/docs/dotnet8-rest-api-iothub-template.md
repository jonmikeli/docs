# .NET 8 REST API IoT Hub Template

This Visual Studio solution template is the result of the experience fo different IoT projects where the creation of such a solution was quite repetitive.

The "Why" of this extension is to cover the need of industrializing the implementation of such solutions, taking advantage of the different experiences and the foundations used to build REST API solutions.

The adopted architecture relies on choices made in the extension this work is based on (REST API Solution Extension, documented [here](dotnet8-rest-api-template.md)).

Choices are based on experiences that might be biased and as a result, the template might have an opinionated perspective.
Feel free to provide feedback and use the template at will.

This template creates a Visual Studio solution with many projects answering to the problems below:
 - expose Azure IoT Hub Service API's technical features
 - build a façade of such features
 - have the possibility to enrich the mentioned features with business aspects (ex: commissioning control, membership controls for different commands, etc)
 - implement customized provisioning mechanisms

From the technical perspective:
 - minimize dependencies
 - implement the most used technical mechanisms like:
    - API Versioning (URL based but it can be updated)
    - exception management
    - logs, traces (configurable Application Insights integration)
    - DI, IoC and mapping factorized configurations
    - test projects injected with the same settings than the projects
    - "layered" approach with a strong focus on the business layer
    - validation mechanisms
    - a fully wired sample of code (database persistence included based on Entity Framework Core and SQL Database)
    - partial test code 
    - automatic documentation (included at OpenAPI level)
    


## Why?

As mentioned above, the "Why" of this extension is to cover the need of templates with something else than pure technical content. "Technical" templates are great but inhere, the idea is to solve another type of need and create a different type of value.

Visual Studio will not generate business code (yet?). The idea is to help developers to maximize the creation of value. Business oriented APIs might be "complex" in certain aspects and generate considerable technical debt if "bad" decisions are made. The extension provides an opinionated canvas to solve the mentioned problems and create a proposal of value.


### A concentrate of "how tos"

Technology evolves fast, very fast. At the same time, developers come from very different paths, some of them not giving time, importance or focus enough to specific topics. Saying that all the needed concepts, principles and patterns are understood, there is still a need to know how to use a given technology stack to implement them. This template tries to help with that.
Of course, the template integrates specific choices when it comes to some practices or ways to solve problems. This is not meant to be the only way to do things, but it is a way that works and that can be used as a starting point.

## Where to find it?

The extension might be found:
 - in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.IoTHubDotNet8RESTAPITemplate?WT.mc_id=AZ-MVP-5004280) (Visual Studio version)
 - in NuGet.org repository [.NET CLI version](https://www.nuget.org/packages/JMI.DotNet8.IoTHub.REST.API.Template.CSharp/?WT.mc_id=AZ-MVP-5004280)

> NOTE
>
> Visual Studio is able now to view and use extensions packaged as NuGet packages. Installing the VSIX (Visual Studio Extension native format) is not necessary if you already have the NUGet package installed.
> The NuGet package might be used either through Visual Studio or .NET CLI.

## How to install it?

### Visual Studio

The extension might be installed from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.IoTHubDotNet8RESTAPITemplate?WT.mc_id=AZ-MVP-5004280).
If the VSIX is downloaded to the local machine, you only need to double-click on it and it triggers the installation process.

The extension can also be installed from the Extensions menu in Visual Studio.

### .NET CLI

The extension might be installed from the [NuGet.org repository](https://www.nuget.org/packages/JMI.DotNet8.IoTHub.REST.API.Template.CSharp/?WT.mc_id=AZ-MVP-5004280) using the following command:

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