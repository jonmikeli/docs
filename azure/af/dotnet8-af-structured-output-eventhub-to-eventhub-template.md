# .NET 8 - Azure Function Solution Template

This Visual Studio solution template is the result of many thoughts after repetitive developments in projects involving data integration (IoT and not IoT).
Its main purpose is to provide a ready to use solution to ingress data, process it and send it to another streaming/messaging service.

The "Why" of this extension is to cover repetitive needs and answer to repetitive questions, choices, etc providing a templatized and industrialized solution.

Choices are based on experiences that might be biased and as a result, the template might have an opinionated perspective.
Feel free to provide feedback and use the template at will.

This template creates a Visual Studio solution with the following characteristics:
 - Azure Function (.NET 8, isolated mode)
 - payload: JSON (it could be changed easily)
 - input: Event Hub
 - output: Event Hub
 - optional outputs:
   - Azure Storage with ingress data
   - Azure Storage with JSON Schema errors


### Azure Function

The extension creates the code for an Azure Function in .NET 8, isolated mode.
However, this code can easily be used to containerize it and use it otherwise.


### A concentrate of "how tos"

Technology evolves fast, very fast. At the same time, developers come from very different paths, some of them not giving time, importance or focus enough to specific topics. Saying that all the needed concepts, principles and patterns are understood, there is still a need to know how to use a given technology stack to implement them. This template tries to help with that.
Of course, the template integrates specific choices when it comes to some practices or ways to solve problems. This is not meant to be the only way to do things, but it is a way that works and that can be used as a starting point.

## Where to find it?

The extension might be found:
 - in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet8AFIsolatedSchemaValidatorIoTOutputsVSTemplateEventHub?WT.mc_id=AZ-MVP-5004280) (Visual Studio version)
 - in NuGet.org repository [.NET CLI version](https://www.nuget.org/packages/JMI.DotNet8.AF.Isolated.SchemaValidator.IoT.StructuredOutputs.EventHub.Template.CSharp/?WT.mc_id=AZ-MVP-5004280)

> NOTE
>
> Visual Studio is able now to view and use extensions packaged as NuGet packages. Installing the VSIX (Visual Studio Extension native format) is not necessary if you already have the NUGet package installed.
> The NuGet package might be used either through Visual Studio or .NET CLI.

## How to install it?

### Visual Studio

The extension might be installed from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet8AFIsolatedSchemaValidatorIoTOutputsVSTemplateEventHub?WT.mc_id=AZ-MVP-5004280).
If the VSIX is downloaded to the local machine, you only need to double-click on it and it triggers the installation process.

The extension can also be installed from the Extensions menu in Visual Studio.

### .NET CLI

The extension might be installed from the [NuGet.org repository](https://www.nuget.org/packages/JMI.DotNet8.AF.Isolated.SchemaValidator.IoT.StructuredOutputs.EventHub.Template.CSharp/?WT.mc_id=AZ-MVP-5004280) using the following command:

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