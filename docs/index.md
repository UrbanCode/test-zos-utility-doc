# Overview

The z/OS Utility plug-in includes steps for retrieving and deploying IBM z/OS artifacts.

This plug-in requires agents that run on the z/OS platform. The Submit Job and Wait For Job steps require the job server component that is included with IBM UrbanCode Deploy, Rational Team Concert, or Rational Developer for System z.

The plug-in includes steps that are related to deploying z/OS artifacts, such as the following steps:

* Copy Artifacts
* FTP Artifacts
* Deploy Data Sets
* Rollback Data Sets
* Cleanup Backup Files

The plug-in also includes steps that are related to running z/OS commands, submitting and tracking jobs, and working with data sets, such as the following steps:

* Submit Job
* Wait For Job
* Run TSO or ISPF Command
* Run MVS Command
* Allocate Data Set
* Copy Data Set
* Replace Tokens MVS

To learn how to import components from data sets in IBM z/OS, see [Deploying to the z/OS platform](https://www.ibm.com/docs/en/urbancode-deploy/7.2.3?topic=integrating-deploying-components-zos-platform).

The plug-in also includes the Generate Artifact Information step, which scans version artifacts and generates text based on a template. The output text can be used as an input property for subsequent steps. Use the Generate Artifact Information to process data sets or members in a component version. You can also use the Generate Artifact Information step to select a set of artifacts to process, by applying filters on data set names, member names, deployment types, and custom properties.

The plug-in also includes steps that are related to managing redundant incremental versions, such as the following steps:

* Remove All Versions
* Remove Redundant Versions

## Compatibility

* IBM UrbanCode Deploy version 7.0.0 or later
* IBM UrbanCode Deploy agents on z/OS
* IBM z/OS version 2.2 or later with System REXX
* Starting with version 49 this plug-in requires Java 8 or above

## Installation

No special steps are required for installation. See [Installing plug-ins in UrbanCode products](https://community.ibm.com/community/user/wasdevops/blogs/laurel-dickson-bull1/2022/06/13/install-plugins). You must install and configure the z/OS deployment tools before you use the plug-in. To learn how to install and configure the z/OS deployment tools, see [Deploying to the z/OS platform](https://www.ibm.com/docs/en/urbancode-deploy/7.2.3?topic=integrating-deploying-components-zos-platform). You must configure the job server component before you run the following steps: Submit Job and Wait For Job.

## History

###  Version 88

* Fixed PH57595 - ROLLBACK DATASET STEP DELETES PDS AFTER DELETING ALL THE NEWLY CREATED MEMBERS DURING DEPLOYMENT
* Minor improvements
* Huge improvements in Rollback Manifest XML file generated during deploy data sets step with backup enabled

###  Version 87

* Added new plugin step - Restore Backup Datasets
* Use Legacy ISPF Gateway to run programs by default

###  Version 86

* Removed support for Submit Job and Wait For Job steps to run outside the mainframe systems
* Fixed APAR PH57188 - SUBMIT JOB INCORRECT FORMATTING WHEN JCL LINE EXCEEDS 72 CHARACTERS

###  Version 85

* Minor improvements in New Package Format Deployment and Deleting Datasets
* Added input to pass Ispf Gateway Path for Deploy Data sets step

###  Version 84

* Fixes output buffering issue when TSO/ISPF command prints too much output.
* Added deployment action filter and new loop type to exclude Deleted missing PDS members
* Fixed a typo with deploy type in generate artifact info step
* Added check for Target Dataset Filter to allow only dataset or member loop types

###  Version 83

* Added new input to enable or disable PDS member replace during deployment
* Fixed issue with cleanup
* Fixed Null Pointer Exception in Generate Artifact information step

###  Version 82

* Fixes CVE-2023-1436 and APAR PH53341 

###  Version 81

* Fixed APAR PH53341 related to parsing error when deploying zOS versions

###  Version 80

* Fixed issue with agent version check and minor improvements

###  Version 79

* Updates deployed artifacts to ZInventory when run on agent versions above 730 

###  Version 78

* Fixes vulnerability CVE-2022-45693 and CVE-2022-45685
* Fixed JMON issue -
  BUZ300E Internal error: Unknown client protocol level.
  FEJ300E Internal error: Unknown client protocol level.

###  Version 77

* Minor improvements
* Fixed issue with deleted containers for generating artifact information

###  Version 76

* Support for deleting members from PDS which is in contention
* Fixes vulnerability CVE-2021-37533

###  Version 75

* Updating jettison library for CVE-2022-40150 CVE-2022-40149

###  Version 74

* Added new step to clean-up backup files 

###  Version 73

* Fixed issue with replacing token for each job and minor improvements

###  Version 72

* Added support for deleting multiple datasets using Delete dataset step
* Fixed security issue CVE-2021-29425

###  Version 71

* TSO ISPF command and FTP Artifacts step migrated to Java
* PH46505 Fixed issue with filtering containers mapped to same Target PDS in Generate Artifact step

###  Version 70

* Wait For Job and MVS Command steps are migrated to Java
* Fixed issue with Java 11 to run shell script

###  Version 69

* Added new step to delete dataset/PDS members

###  Version 68

* Update udclient and uDeployRestClient
* Fixed issue with GDG version creation in Allocate Steps

###  Version 67

* Minor improvements.

###  Version 66

* Remove All Versions and Remove Redundant Versions steps are migrated to run on Java for performance improvements.
* Added checkbox for Dry run in Remove All Versions step.

###  Version 65

* Copy Artifacts and Copy Data Set steps are migrated to run on Java for performance improvements.

###  Version 64

* Remove log4j functionality related to: CVE-2019-17571, CVE-2020-9488. CVE-2021-4104, CVE-2022-23302, CVE-2022-23305, CVE-2022-23307

###  Version 63

* Minor enhancements in Submit Job and Wait For Job steps
* Fixed handling of temporary datasets in case of failure in new package format
* Minor Improvments in new package format
* Fixed ZFileException while cleaning up unclosed temporary dataset
* Fixed IGD17036I in new package deployments

###  Version 62

* Added check box to delete dataset if already exist for Allocate steps

###  Version 61

* Allocate data set steps are rewritten in Java for better performance

###  Version 60

* Enhancements and bug fixes for HFS deployment and rollback – APAR PH42431