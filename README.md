# Azure Maze #
Kinetic Maze, with the Azure Kinect instead of XBox Kinect.



## Installation ##
Instructions to install the Azure Kinect SDK are from microsoft, copied here for convinience. No other dependencies should be needed.

1. Configure the Microsoft Package Repository, and install the Azure Kinect packages (tools, headers, and body tracking):
```
 curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
 sudo apt-add-repository https://packages.microsoft.com/ubuntu/18.04/prod
 sudo apt-get update
 sudo apt install k4a-tools
 sudo apt install libk4a1.1-dev
 sudo apt install libk4abt1.0-dev
```
Note: requires OpenGL 4.4 and above

When installing samples:
https://github.com/microsoft/Azure-Kinect-Sensor-SDK/issues/896


## Azure Kinect on Linux ##
As most Microsoft documentation is windows based, Linux usage will be documented as thoroughly as possible for future use. In general, follow instructions in the Microsoft documentation.

To launch the Azure Kinect Viewer, run `k4aviewer` in the command line.

## Project Info ##
C tracker code is mostly pulled from Microsoft sample code.

Current plan: Create two FIFO pipes, one for image data and one for joint (aka hand angle) data. Then figure out how to access those from python, or another C program. May want to convert entire project to C, but unlikely.

Joint info is priority, to get project back to basic working state on new hardware.



## Reference Links ##
[Azure Kinect Samples](https://github.com/microsoft/Azure-Kinect-Samples)
[Azure Kinect SDK](https://github.com/microsoft/Azure-Kinect-Sensor-SDK)
[Azure Kinect DK Documentation](https://docs.microsoft.com/en-us/azure/kinect-dk/)

[Body Tracking SDK Reference](https://microsoft.github.io/Azure-Kinect-Body-Tracking/release/1.x.x/index.html)
[Azure Kinect Sensor SDK Reference](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/index.html)
