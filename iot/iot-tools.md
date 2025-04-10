# IoT Tools

This section enumerates some of the tools that I have been building for IoT and Azure (PaaS) solutions. The spirit of the whole set of tools is to:
 - ease developers' life
 - simplify and ease the first steps
 - accelerate development
 - increase quality
 - absorb a certain level of complexity
 - industrialize and streamline the development process



Accelerators: 2

Simulators: +10

Extensions: 14

Libraries: 5

## Accelerators

The accelerators have for purpose to increase the productivity of specific tasks. For now, accelerators are mainly technical even though they provide different types of value.

### IoT Accelerator

The IoT Accelerator takes in charge the deployment of the infrastructure or the platform components of an IoT Solution. Inherently, the produced content remains quite technical but this is what is expected at this level.

This tool is not available for a public use now.
After some unappropriated uses, it has been retired from public access. A commercial version is being considered instead.

### Others

Other types of accelerators have been under work. They will be published when the value the provide will be good enough and/or meaningful. For now, they are only technical facilitators for specific tasks.

## Simulators

Not sure there is a clear definition of what to expect behind a "simulator".
So, it is probably useful to state what the simulators are in the context of this content.

Simulators are applications being able to reproduce most of the IoT flows and interactions (D2C and C2D).
These simulators do not include rich data simulation features. Instead, they contain very simple components to randomize data from the technical perspective.

The mentioned simulators are delivered through two formats
    - containerized application
    - standalone application (mobile application)
  
### Containerized

The containerized simulator is the initial and default version of the simulator. It is the richer and more versatile type of built simulator here.
It finds its place in projects that need different IoT simulated devices running autonomously.
Similarly to the accelerator mentioned previously, the containerized version of the simulator as been made private to protected the work against unethical use.

### Mobile app

A [mobile application simulating](https://techcommunity.microsoft.com/t5/internet-of-things-blog/transform-your-phone-into-an-iot-device-with-net-maui/ba-p/3673909?WT.mc_id=AZ-MVP-5004280) most of the IoT flows has been implemented too.

You can fin the details [here](https://techcommunity.microsoft.com/t5/internet-of-things-blog/transform-your-phone-into-an-iot-device-with-net-maui/ba-p/3673909?WT.mc_id=AZ-MVP-5004280).

This initial application has been completed with another one, taking into account [Teltonika's Codec 8E](https://wiki.teltonika-gps.com/view/Codec) format (Hex).
This version includes the possibility to simulate coherent GPS data (routes, paths, position and speed in time), based on Azure Maps.


## Extensions

A set of extensions complete the different tools and accelerators described in this content.
The extensions described in this section are declined in two versions:
 - Visual Studio version
 - .NET CLI version

The provided links target the last existing version. Most of the provided extensions have been declined in different .NET versions.

### EH to SB

#### Description

Solution template extension to create an Azure Function reading messages from an Event Hub, implementing some processing (validations, etc) and pushing the messages to a Service Bus.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet7AFSchemaValidatorIoTOutputsVSTemplateServiceBus)
 - [.NET CLI](https://www.nuget.org/packages/JMI.DotNet7.AF.SchemaValidator.IoT.StructuredOutputs.ServiceBus.Template.CSharp/)


### EH to EH


#### Description

Solution template extension to create an Azure Function reading messages from an Event Hub, implementing some processing (validations, etc) and sending the messages to a new Event Hub.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet7AFSchemaValidatorIoTOutputsVSTemplateEventHub)
 - [.NET CLI](https://www.nuget.org/packages/JMI.DotNet7.AF.SchemaValidator.IoT.StructuredOutputs.EventHub.Template.CSharp/)

### EH to SR

#### Description

Solution template extension to create an Azure Function reading messages from an Event Hub, implementing some processing (validations, etc) and sending the messages to SignalR.

#### Links

 - [Visual Studio]()
 - [.NET CLI]()

### EH to DT

#### Description

Solution template extension to create an Azure Function reading messages from an Event Hub, implementing some processing (validations, etc) and sending the messages to Digital Twins.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet7AFDigitalTwinsVSTemplate)
 - [.NET CLI](https://www.nuget.org/packages/JMI.DotNet7.AF.DigitalTwins.Template.CSharp/)

### IoT Hub facade

#### Description

Solution template extension to create an IoT Hub facade, based on the REST API (WebAPI) extension, following structured and layered solutions.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.IoTHubDotNet7RESTAPITemplate)
 - [.NET CLI](https://www.nuget.org/packages/JMI.DotNet7.IoTHub.REST.API.Template.CSharp/)

### YARP Reverse proxy

#### Description

Solution template extension to create an reverse proxy (YARP) with common configurable settings.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet8YARPVSTemplate)
 - [.NET CLI](https://www.nuget.org/packages/JMI.Net8.Gateway.Template.CSharp/)

### REST API

#### Description

Solution template extension to create an REST API (WebAPI) following structured and layered solutions.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet7RESTAPIVSTemplate)
 - [.NET CLI](https://www.nuget.org/packages/JMI.DotNet7.REST.API.Template.CSharp/)

### gRPC

#### Description

Solution template extension to create an gRPC services with default and common settings.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.DotNet7gRPCAPIVSTemplate)
 - [.NET CLI](https://www.nuget.org/packages/JMI.DotNet7.GRPC.API.Template.CSharp/)

### Azure IoT Edge

#### Description

Solution template extension to create an IoT Edge solution with common setting and slightly improved structure.

#### Links

 - [Visual Studio](https://marketplace.visualstudio.com/items?itemName=JonMikelInza.AzureIoTEdgeDotNet6CSharpVSTemplate)
- [.NET CLI](https://www.nuget.org/packages/JMI.IoT.Edge.DotNet6.CSharp.Template.CLI/)

### Data simulation

#### Description

Library containing simple logic to randomize data after a JSON schema definition.

#### Links

 - [.NuGet](https://www.nuget.org/packages/JMI.JSON.Data/)
