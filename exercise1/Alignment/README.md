# MyMauiApplication

This is a sample application for the .NET Maui platform.

Set up based on <https://rjj-software.co.uk/blog/building-net-maui-android-apps-on-linux-based-operating-systems/>

## Prerequisites

Install the .NET 7 SDK as described here: <https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu#2004->
Install Android Studio as described here: <https://developer.android.com/studio/install>
Create a virtual device as described here: <https://developer.android.com/studio/run/managing-avds>

## Getting Started

Install the .NET Maui workload:

```bash
sudo dotnet workload install maui-android
```

Create a .NET Maui project:

```bash
dotnet new maui -n MyMauiApplication
cd MyMauiApplication
```

## Building

```bash
dotnet build
```

## Start Android Debug Brigde (adb) server

Start adb server:

```bash
adb start-server
```

## Running on a virtual device

List and start available devices:

```bash
emulator -list-avds
emulator -avd Pixel_6_API_27
```

In another terminal, run the application:

```bash
dotnet build -t:Run -f net7.0-android
```
