# Overview

The z/OS Dataset Writer plug-in copies text, dataset, or USS file to a mainframe dataset.

Apart from copying content to a mainframe dataset, this plug-in provides the following features:

* Allocates a new output dataset with the required parameter.
* Deletes the existing output dataset to create a new one with desired parameters.

## Compatibility

The plug-in is compatible with:

* UrbanCode Deploy version 7.0.0 or later
* UrbanCode Deploy agents on z/OS
* IBM z/OS version 2.1 or later
* IBM Java 8 or 11

## Installation

No special steps are required for installation. See [Installing plug-ins in UrbanCode products](https://community.ibm.com/community/user/wasdevops/blogs/laurel-dickson-bull1/2022/06/13/install-plugins).

## History

### Version 4

* Enhancement to accept multiple datasets or files as input
* Minor Improvements
* Fixed security issue CVE-2021-29425
* Fixed Jettison Vulnerability

### Version 3

!!! Note 
    while upgrading plugin from older versions to version 3 
    Sequential output dataset must be enclosed in single quotes for a fully qualified dataset. 
    If the single quotation marks are omitted, the user’s dataset prefix from the TSO profile is 
    automatically appended to the front of the dataset name.

* Enhancement to accept source as PDS member or sequential dataset or USS File

### Version 2

* Fixed issue with GDG version creation

### Version 1

* Initial release