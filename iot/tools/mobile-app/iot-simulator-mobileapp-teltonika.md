# Azure IoT Simulator - Mobile application - Teltonika

This version of the mobile application is based on the [Azure IoT Simulator - Mobile application](iot/tools/mobile-app/iot-simulator-mobileapp.md).
As the title suggests, this new version is designed to include features specific to Teltonika's contexts.

## Features

The Teltonika version of the mobile application includes the following features:
 - telemetry based on Teltonika's Codec 8E
 - (optional) coherent random GPS data

### Telemetry (Codec 8E)

This initial version creates telemetry messages with a fixed set of properties.

TODO
Describe them

These properties are serialized in a HEX string, following the Codec 8E format.


### GPS data

When it comes to routes or paths, it might be helpful to generate coherent GPS data. By "coherent" we mean meaningful data in terms of:
 - position (ordered)
 - speed
 - time
 - according to a route

This version of the application uses Azure Maps to implement part of the feature.
Required credentials are configurable in the application.