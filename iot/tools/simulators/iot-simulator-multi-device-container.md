# Azure IoT Device Simulator (.NET 8, C#) - Multi device

## New features
This version of the Azure IoT Device Simulator implements provisioning relying on DPS (Device Provisioning Service).
It implements provisioning based on **group enrollment** with:
   - symmetric keys
   - CA X509 certificates

Individual enrollments are not covered.

## Description
The implementation of this simulator is not simply a regular simulator with DPS capabilities.
All the provisioning process has been coded to add new configuration possibilities keeping in mind enterprise oriented use cases.

You can find the whole detailed documentation [here](https://github.com/jonmikeli/azureiotdevicesimulator8-dps-multidevice).


*Azure IoT Device Simulator logs*

![Azure IoT Device Simulator Logs](docs/images/IoTSimulator-DPS-CAX509.gif)


## IoT tools
This simulator keeps the spirit of the [regular version](https://github.com/jonmikeli/azureiotdevicesimulator5).
It completes other simulators like:
 - [regular version of the simulator](https://github.com/jonmikeli/azureiotdevicesimulator5)
 - [Plug and Play version of the simulator](https://github.com/jonmikeli/azureiotdevicesimulator5-pnp) (based on DTDL v2)
 - DPS version (this repository)

I guess that forking this version with IoT Plug and Play capabilities may be a good next step.

## Automatization
A script is provided in the repository to showcase how to create a set of simulators (containerized version).
The sample creates the containers in the local machine. You can use the same mecanism and adapt it to cloud services like ACR and ACI.

The whole set of simulated devices may be provisioned and running in a few seconds.....literally. Once the initial settings are configured (configuration files), everything runs automatically (provisioning, modules, telemetries, D2C/C2D flows, etc).

Telemetry messages are based on the templates used in the regular simulator.

## Examples of use
 - development tool for developers working on Microsoft Azure IoT solutions (cloud).
 - tester tool in IoT-oriented projects.
 - scalable IoT simulation platforms.
 - complete and configurable D2C (data and reported properties) and C2D (direct methods, desired properties, messages, jobs, etc).
 - etc

## Technical information
 - .NET 8 (C#)
 - Microsoft Azure IoT SDK (provisioning, properties, tags, C2D/D2C, device modules*).
 - Docker and bash for the containerized use cases.

## Global features
 - device provisioning (group enrollment with symetric keys).
 - device provisioning (group enrollment with CA X509 certificate).
 - provisioning configuration through environment variables, command parameters or setting files.
 - device level simulation (C2D/D2C).
 - module level simulation (C2M/M2C).
 - device simulation configuration based on JSON files.
 - module simulation configuration based on JSON files.
 - no specific limitation on the number of modules (only limited by Microsoft Azure IoT Hub constraints).
 - containerizable.
 - message generation based on JSON Schemas. The simulator includes different types of messages (telemetry, error, commissioning). The structure of each message is defined by configurable JSON Schemas.
 - implementation of full IoT flows (C2D, D2C, C2M, M2C).

See below for more details.

## Functional details

### Device level (C2D/D2C)

*Provisioning*


The implemented provisioning relies on [Azure IoT Hub Device Provisioning Service](https://docs.microsoft.com/en-us/azure/iot-dps/).
The simulated device calls the DPS with the provided configuration and gets an Azure IoT Hub connection string according to the policies configured in the DPS.

The simulator has been designed to work in different provisioning use cases:
 1. If the simulator has no connection string, a provisioning process is initiated.
   This process requires a DPS configuration to be set.
   The DPS configuration can be provided by:
    - environment variables (recommended and useful for containerized targets. It is less prone to compromise security.).
    - command line parameters, that will overwrite the environment variables (may be used in not containerized targets, in automated processes and providing safe ways to instantiate the simulator).
    - if none of the previous settings are found, a `dpssettings.json` file will be loaded (not recommended in production unless the JSON file is persisted in a secured location. This third alternative can be used as a development tool.).
 2. If the simulator finds a connection string, it uses and it skips the provisioning process.
 
> NOTE
>
> With symmetric key authentication type, the `device id` can be set through an environment variable too. This allows easier scripted provisioning scenarios (ex: loop to create a set of simulated devices). With X509 certificates, the `device id` is located inside the certificate.

> NOTE 2
>
> The different authentication types require different parameters. The details about how to set the different DPS settings are described in the detailed documentation.

*Commands implemented by default*
 - request latency test
 - reboot device
 - device On/Off
 - read device Twin
 - generic command (with JSON payload)
 - generic command
 - update telemetry interval

 
 *Messages*


 D2C: The device can send messages of different types (telemetry, error, commissioning).
 
 C2D: Microsoft Azure IoT Hub can send messages to a given device.

 
 *Twin*


 Any change in the Desired properties is notified and handled by the device.

 The device reports changes in different types of information to the Microsoft Azure IoT Hub.


### Module level (C2M/M2C)
The features at the module level are the identical to the device features except for the latency tests.

> NOTE
>
> The security type implemented for module identities is based on symmetric keys. Depending on the faced use cases, additional possibities may be added in upcoming versions. Adding X509 module identities will require to add the needed certificates in a secured way (to the cloud and the device).
> Personnally, I am wondering why a given device and its module identities could implement different types of security. What requirements may lead to such a scenario?


  
## Global technical features

Functional features are based on these generic technical features:
 - device provisioning and reprovisioning.
 - telemetry sent from a device.
 - a device can contain one or many modules.
 - each module behaves independently with its own flows (C2M/M2C) and its configuration settings.
 - the device that contains the modules has its own behavior (based on its own configuration file).
 - telemetry sent from a module.
 - messages received by a device.
 - messages received by a module.
 - commands received by a device.
 - commands received by a module.
 - Twin Desired properties changed notification (for devices).
 - Twin Desired properties changed notification (for modules).
 - Twin Reported properties updates from a device.
 - Twin Reported properties updates from a module.


### D2C
#### Device level
 - IoT Messages
 - Twins (Reported)

#### Module level (M2C)
 - IoT Messages
 - Twins (Reported)

### C2D
#### Device level
 - Twins (Desired)
 - Twins (Tags)
 - Direct Methods
 - Messages

#### Module level (C2M)
 - Twins (Desired)
 - Twins (Tags)
 - Direct Methods
 - Messages

## Upcoming features
- ~~adding IoT Plug and Play (DTDL v2)?~~
- tools to create PKIs

## More information
Detailed documentation [here](https://github.com/jonmikeli/azureiotdevicesimulator8-dps-multidevice).