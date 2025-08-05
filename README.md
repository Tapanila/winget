# SharpCaster MSI Installer

This repository contains a WiX Toolset project that creates MSI installers for [SharpCaster](https://github.com/Tapanila/SharpCaster).

## Features

- Automatically fetches the latest SharpCaster release
- Creates universal MSI installer supporting both x64 and ARM64 architectures
- Automated daily builds via GitHub Actions
- Installs desktop and start menu shortcuts
- Automatically detects system architecture and installs the correct executable

## GitHub Actions Workflow

The workflow runs daily and:

1. Checks for the latest SharpCaster release
2. Downloads both Windows x64 and ARM64 executables
3. Creates a universal MSI installer using WiX Toolset 6.0
4. Publishes the MSI as a GitHub release

## Manual Build

To build manually:

1. Install .NET 6.0 SDK
2. Install WiX Toolset: `dotnet tool install --global wix --version 6.0.1`
3. Download both `sharpcaster-win-x64.exe` and `sharpcaster-win-arm.exe` to the project root
4. Build: `dotnet build SharpCaster.wixproj -c Release`

## Installation

Download the latest MSI from the [Releases](../../releases) page and run it to install SharpCaster.