# Developement envrionement configuration
How to configure everything

## Visual Studio 2017
The project needs to be opened with visual studio 2017. The project targets Windows 10 Build 1703, the Creators Update, it need to be installed in order to run. The apropriate SDKs also need to be installed in visual studio.

Since Visual Studio 2017 it is much easier to select and install packages for Visual Studio. Using the installer, we can install the packages required for developement. Selecting the Universal Windows Platform on the Workload page will select most of the packages we need. Then on the individual packages page, we need to select some more if they are not already selected.

* Target pack for .NET portable libraries
* Target pack for .NET 4.6.1
* Windows 10 SDK 10.0.15063 for UWP (C# version minimum)

In order to deploy the application in developpement, the dev mode must be enabled on windows. If visual studio doesn't asked to activate [follow this guide](https://docs.microsoft.com/en-us/windows/uwp/get-started/enable-your-device-for-development).

### Important
The key included in the project MarkdownEditor called MarkdownEditor_TemporaryKey.pfx is important. It's the public private key used to publish the application in devlopement mode. **It should never be replaced**. It might be required to install it on one's computer in order to be able to deploy the application after compiling. **Simply install the certificate**, it does not require a password.

### Extensions

#### [Automatic Versions](https://marketplace.visualstudio.com/items?itemName=PrecisionInfinity.AutomaticVersions)
This extension allows incrementation of the assembly build info automatically when using the option in the build menu inside visual studio. See [Versions](#versions) for explanation on build numbers and revision numbers.

## Versions
Rules for versionning are as follows. Major, Minor, Build, Revision. Major should increment when big changes in scope occur, new platform, major feature set. Minor should increment when substantial feature set is added, many features. Build is incremented by release, each feature or group of feature release. Revision should be incremented each time a commit or set of commits is made, *each successfull build worthy of being tested*. Unit tests should follow major, minor and build numbers but their incrementation should follow addition of new tests only.

## Git
It is recomended to use either git from the command line or a good git GUI application such as gitkraken. The Github desktop application is not ideal and is missing a lot of features.