# openIMIS - IMIS Assign Photo Windows Service

The openIMIS IMIS Assign Photo Windows Service is a service which is executed 
periodically and associates the photos sent by the mobile apps through FTP to the 
corresponding insurees.
It is built as Windows service, running in the background. 

## Getting Started

These instructions will get you a copy of the project up and running on your local 
machine for development and testing purposes. See deployment for notes on how to 
deploy the project on a live system.

### Prerequisites

In order to use and develop the openIMIS IMIS Assign Photo Windows Service on your local 
machine, you first need to install:

* [openIMIS Database](https://github.com/openimis/database_ms_sqlserver)
* [openIMIS Web Application](https://github.com/openimis/web_app_vb) (optional, 
but facilitates the insuree registration for testing of this component)

### Installation

To make a copy of this project on your local machine, please clone the repository.

```
git clone https://github.com/openimis/imis_assign_photo_service_vb
```

Then build the solution in Visual Studio.

With administrator priviledge, install the Windows service via the following command: (For the 64-bit version of the .NET Framework 4 or 4.5.*, the default path is C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe.)

```
InstallUtil AssignPhotoService.exe
```

At this stage, the service is running on the local machine. In order to configure when and on which database the service should run, the Controller application should be used as follow:

- Copy the file .\AssignPhotoController\bin\Debug\AssignPhotoController.exe into the same folder as AssignPhotoService.exe and AssignPhotoService.exe.config which is by default: .\AssignPhotoService\bin\Debug.
- Open the Controller application AssignPhotoController.exe.
- From the system tray, right click on the Assign Photo icon.
- In the new window, enter the database details and time details for the service to run.
- Apply the changes.
- Restart the service.

## Deployment

For deployment please read the 
[installation manual](https://openimis.readthedocs.io/en/latest/web_application_installation.html#install-windows-services).

## Built With

* [Visual Studio](https://visualstudio.microsoft.com/) 

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/openimis/imis_assign_photo_service_vb/tags). 

<!--## User Manual 

The user manual can be read on [openimis.readthedocs.io](http://openimis.readthedocs.io/en/latest/user_manual.html).
-->

## License

Copyright (c) Swiss Agency for Development and Cooperation (SDC)

This project is licensed under the GNU AGPL v3 License - see the [LICENSE.md](LICENSE.md) file for details.
