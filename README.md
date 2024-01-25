# test-zos-utility-doc

## Pre-requisites
* Python along with pip installed
* VSCode or any other IDE installed

## Build process steps
* Checkout code from Github to local system 
* Create virtual environment using command `python -m venv venv`
* Activate virtual environment using command `.\venv\Scripts\Activate.ps1` for `Windows` and `source venv/bin/activate` for `Mac/Linux`
* Install mkdocs using command `pip install mkdocs-material`
* Make necessary changes for the documentation
* Command `mkdocs serve` will host the documentation changes on local host
* After completion of changes and testing. Deactivate virtual environment using command `deactivate venv`
