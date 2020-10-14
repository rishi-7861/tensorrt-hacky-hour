# TensorRT Applications


This alwaysAI applications set use TensorRT binaries to do the local infernecing on a NVIDIA Jetson device, these binaries can be found in the alwaysAI model catalog.  The model will start with TRT and end with the Jetson device name it should be run on, for example nano.  These binaries are the most efficient way to do infernecing on NVIDIA Jetson device achieving infernecing times of 9 milliseconds on some devices.  Currently alwaysAI support TensorRT binaries for Jetson Nano, TX2 and Xavier XM.    


## Repo Programs
| Folder                     	| Description                                                                                              	|
|----------------------------	|----------------------------------------------------------------------------------------------------------	|
| license-vehicle-detection   | Program detects vehicles and license plates, currently setup to work with Jetson Nano|
| distance-between-hands 	    | Program detections distance between hands in meters, this application needs a Intel Realsense camera to run and is setup to work with Jetson Nano|


## Setup

This app requires an alwaysAI account. Head to the [Sign up page](https://www.alwaysai.co/dashboard) if you don't have an account yet. Follow the instructions to install the alwaysAI tools on your development machine.

Next, create an empty project to be used with this app. When you clone this repo, you can run `aai app configure` within the repo directory and your new project will appear in the list.

## Usage

Once the alwaysAI tools are installed on your development machine (or edge device if developing directly on it) you can run the following CLI commands:

To set up the target device & install path

```
aai app configure
```

To install the app to your target (make sure you use the aai app models add command to add the current TensorRT model)

```
aai app install
```

To start the app

```
aai app start
```
