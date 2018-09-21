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

### Installing

To make a copy of this project on your local machine, please clone the repository.

```
git clone https://github.com/openimis/imis_assign_photo_service_vb
```

You can then build the solution.

To execute the service and the associated controller, the Windows Administrator 
account is required. 

To start the Windows service execute the following command:

```
InstallUtil AssignPhotoService.exe
```

For the 64-bit version of the .NET Framework 4 or 4.5.*, the default path is
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe .

All configuration (database connection, schedule) is donned by using the Controller
application, within the Settings form found by opening the menu from the task tray. 

To start the Controller application execute the following command:

```
AssignPhotoController.exe
```

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
