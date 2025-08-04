# YPF-Manager

fork version of [YPF-Manager](https://github.com/Xorboth/YPF-Manager)，provides a prebuilt executable. You can download the latest release from [Releases](https://github.com/lxl66566/YPF-Manager/releases).

## Compile Guide

This guide explains how to compile the YPF-Manager project.

### Prerequisites

- **.NET Framework 4.7.2 Developer Pack**

### Steps to Compile

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/lxl66566/YPF-Manager.git
    cd YPF-Manager
    ```
2.  **Download and extract DotNetZip:**
    ```bash
    curl -L -o DotNetZip.1.15.0.nupkg https://www.nuget.org/api/v2/package/DotNetZip/1.15.0
    mkdir -p "packages/DotNetZip.1.15.0/lib/net40"
    tar -xf DotNetZip.1.15.0.nupkg -C "packages/DotNetZip.1.15.0" lib/net40/DotNetZip.dll
    ```
3.  **Build the Solution:**
    ```bash
    msbuild "YPF Manager.sln" /p:Configuration=Release /p:Platform="Any CPU"
    ```
4.  **Find the Executable:**
    The compiled executable (`YPF Manager.exe`) and its dependencies (like `DotNetZip.dll`) will be located in the `YPF Manager\bin\Release` (or `Debug`) directory.
