# .NET 10 gRPC Template

This Visual Studio solution template is the result of different works on how to help developers when it comes to developing services. It includes the solution to many problems faced in real-life projects as well as the will to follow a certain level of good practices.

The created template is less elaborated than those created for REST APIs.
Richer templates for gRPC services will come with time, depending on the experiences and feedback from users.

The "Why" of this extension is to simplify developers' lives and help them to find easy ways to implement basic features, with patterns and good practices, without having to spend a lot of time looking for "how tos". The extension absorbs that work and offers it to developers.

IDEs come with full of technical templates. However, I thought it could be meaningful to create value with deeper approaches and help developers in their daily work.

Choices are based on experiences that might be biased and as a result, the template might have an opinionated perspective.
Feel free to provide feedback and use the template at will.

This template creates a Visual Studio solution implementing the features below:
 - minimize dependencies
 - configurable reflection
 - configurable JSON transcoding
 - configurable OpenAPI


## Why?

As mentioned above, the "Why" of this extension is to cover the need of templates with something else than pure technical content. "Technical" templates are great but inhere, the idea is to solve another type of need and create a different type of value.

Visual Studio will not generate business code (yet?). The idea is to help developers to maximize the creation of value.
Also, the IT environment changes fast and widely. It might end being very time consuming starting to be productive with new technologies. This extension tries to save some time providing solutions from the real world and based on good practices.


### gRPC APIS?

After RPC, SOAP and many other binary (proprietary) services, it was the time of REST APIs (mainly JSON).
THey brought kind of "simplicity", cross-platform and a sort of "efficiency". This said, it also came with missing features and some performance drawbacks compared to other types of services.
The natural evolution leads us to gRPC, with binary serialization and way more efficient than REST JSON APIs.
The development mode is a bit more complex than REST API's but this is another reason why this extension was built and released.

## Where to find it?

The extension might be found:
 - in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet10gRPCAPIVSTemplate?WT.mc_id=AZ-MVP-5004280) (Visual Studio version)
 - in NuGet.org repository [.NET CLI version](https://www.nuget.org/packages/JMI.DotNet10.GRPC.API.Template.CSharp/?WT.mc_id=AZ-MVP-5004280)

> NOTE
>
> Visual Studio is able now to view and use extensions packaged as NuGet packages. Installing the VSIX (Visual Studio Extension native format) is not necessary if you already have the NUGet package installed.
> The NuGet package might be used either through Visual Studio or .NET CLI.

## How to install it?

### Visual Studio

The extension might be installed from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet10gRPCAPIVSTemplate?WT.mc_id=AZ-MVP-5004280).
If the VSIX is downloaded to the local machine, you only need to double-click on it and it triggers the installation process.

The extension can also be installed from the Extensions menu in Visual Studio.

### .NET CLI

The extension might be installed from the [NuGet.org repository](https://www.nuget.org/packages/JMI.DotNet10.GRPC.API.Template.CSharp/?WT.mc_id=AZ-MVP-5004280) using the following command:

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