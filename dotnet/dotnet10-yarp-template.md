# .NET 10 YARP Template

This Visual Studio solution template is the result of different works on how to help developers when it comes to developing distributed applications (backend). It is quite common to implement a gateway (or many) in such solutions. This extensions helps in that task and provides a starting point to implement a gateway using YARP (Yet Another Reverse Proxy).

The created template implements a quite simplistic but complete (and operational) solution.
It includes common settings and a configuration by default that can be updated afterwards.

The "Why" of this extension is to simplify developers' lives and help them to find easy ways to implement basic features, with patterns and good practices, without having to spend a lot of time looking for "how tos". The extension absorbs that work and offers it to developers.

IDEs come with full of technical templates. However, I thought it could be meaningful to create value with deeper approaches and help developers in their daily work.

Choices are based on experiences that might be biased and as a result, the template might have an opinionated perspective.
Feel free to provide feedback and use the template at will.


### YARP

YARP is a reverse proxy, used in many Microsoft products, that allows to create a gateway to expose multiple services through a single access endpoint. It is a great solution to create a gateway for a microservices architectures.

It includes features like:
 - Swagger UI
 - Health checks
 - Routing
 - Request Logging
 - Rate limiting
 - Caching
 - Compression
 - Request and response transformations
 - Request and response tracing
 - Protocol translation
 - Load balancing
 - etc

More information about [YARP](https://microsoft.github.io/reverse-proxy/?WT.mc_id=AZ-MVP-5004280).

## Where to find it?

The extension might be found:
 - in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet10YARPVSTemplate?WT.mc_id=AZ-MVP-5004280) (Visual Studio version)
 - in NuGet.org repository [.NET CLI version](https://www.nuget.org/packages/JMI.Net10.Gateway.Template.CSharp/?WT.mc_id=AZ-MVP-5004280)

> NOTE
>
> Visual Studio is able now to view and use extensions packaged as NuGet packages. Installing the VSIX (Visual Studio Extension native format) is not necessary if you already have the NUGet package installed.
> The NuGet package might be used either through Visual Studio or .NET CLI.

## How to install it?

### Visual Studio

The extension might be installed from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet10YARPVSTemplate?WT.mc_id=AZ-MVP-5004280).
If the VSIX is downloaded to the local machine, you only need to double-click on it and it triggers the installation process.

The extension can also be installed from the Extensions menu in Visual Studio.

### .NET CLI

The extension might be installed from the [NuGet.org repository](https://www.nuget.org/packages/JMI.Net10.Gateway.Template.CSharp/?WT.mc_id=AZ-MVP-5004280) using the following command:

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