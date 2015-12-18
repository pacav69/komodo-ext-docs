[[_TOC_]]

# How to: Create a Komodo Extension
This document describes how to create a Komodo Extension.

If Komodo developer extension is not installed the go here first -
[komodo-developer-extension](http://komodoide.com/packages/addons/komodo-developer-extension/)

## Create extension
To create an extension select from the menu Project-->New from template-->Create Komodo Extension
This will then open up a window to select a working directory where the project files will be generated and stored.
It will then open up a new windows titled 'Welcome to the New Komodo Extension'

![New Komodo Extension](http://i.imgur.com/jsYWFtZ.png)


## Description of the New Komodo Extension dialog window

- Name: The Name of the project.
The name is derived from the project name that was used to start the project.



- Version: The version that will be used to identify the project level. 
I suggest that you use the Semantic Versioning 2.0.0 system. Starting at 0.0.1

As described by the documentation 
Given a version number MAJOR.MINOR.PATCH, increment the:

- MAJOR version when you make incompatible API changes,
- MINOR version when you add functionality in a backwards-compatible manner, and
- PATCH version when you make backwards-compatible bug fixes.
- Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

More information can be found [here ](http://semver.org/)


- Description: Give a description of the project as this is what will appear in the extensions/add-on page of the completed extension.
- Author: You full name.
- Domain: this is the unique identifier if you don't have one then i suggest that you use ActiveState.com.
- Home Page: is the location of the extension.
- Extension Id: is the unique identifier that is combination of the domain and the extension name.

Once completed click on next and it will display a new windows with instructions

![Completing the New Komodo Extension](http://i.imgur.com/Dv2TSyA.png)

# Komodo Extension Development Macros
There are several macros that are installed when creating a Komodo Extension:

## Build
This macro will build and create an xpi file of the project

## Build and install
This macro will build and create an xpi file of the project as well as install it  on Komodo. Note that this will require a restart of Komodo.

## Reconfigure
This will allow changes to be made to the install.rdf file.

## Docs_-_Extensions
This will open up the help file to explain Komodo Extensions


# Komodo Extension Development tools

These can be found under the menu tools-->Extension Developer
## Using the tools

### Extension Developer


### Enable debugging  preferences

### JavaScript shell

### JavaScript Environment

### JavaScript injector

### Pyshell

### HTML Editor

### Xul editor

### Reg Exp Evaluator

### Interactive Xpath Tester
