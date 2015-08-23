# Welcome to the Komodo-Joomla-builder wiki!
# Komodo Joomla Builder
## Description
Create a Joomla project infrastructure using Komodo and Grunt.

## References
[Developer Mozilla: Add-ons](https://developer.mozilla.org/en-US/Add-ons/SDK/Tutorials)

## Background
This project is based on Komodo's Extension Generator where it would create a project file in a project directory and then populate the directory with Komodo's extension file structure with prompts to the user to input information for extension details and creating a manifest file with accompanying macros to modify the manifest file, build the extension and build and install the extension to Komodo.

## Project Scope
With this project it will do a similar procedure in combination with GruntJS, plugins and Komodo macros to create the Joomla infrastructure, with the ability to modify and add Joomla files and functions, do syntax checks, ensure compliance with Joomla coding standards, use autocomplete for Joomla coding.

## What is Joomla?
Joomla is an award-winning content management system (CMS), which enables you to build Web sites and powerful online applications. Many aspects, including its ease-of-use and extensibility, have made Joomla the most popular Web site software available. Best of all, Joomla is an open source solution that is freely available to everyone.
More information can be found [here](http://www.joomla.org/)

## What are the parts of Joomla?

### Component

### Plugin

### Templates

## Workflow
## Download Komodo Joomla Builder
After downloading and installing the Komodo Joomla builder file (Work In Progress (WIP))

## Joomla naming convention
Joomla requires that the naming convention of files and functions be consistent throughout the project to utilise the Joomla infrastructure.

### Building Joomla component procedure
The first time the developer uses the builder they are prompted for default parameters.
Such as author name, email, url etc this information is stored in a config file for later reference.
It then displays a project help information outlying the workflow.

It does a check for global nodejs installation and prompts if not installed as this is required for grunt
then checks for global grunt installation and prompts if not installed.

## Macros and their functions
### Komodo Extension - Create Joomla Project Macros.
* Create project, this adds macros to the Joomla project.
* Modify User data, this modifies the user data that is used as default parameters.
* Modify default Grunt parameters, Modify settings for Grunt.
* Modify Grunt Plugins parameters, Modify settings for Grunt Plugins.
* Add other plugins, add user defined plugins to grunt list.
* Help, Local help file of how to use the builder.

### Create Project macro flow
* User selects 'Create project' macro
* User then selects type of project: a component, plugin or template
* default parameters are read and displayed
* user adds additional information
* user selects project directory
* the builder checks for local nodejs
* then checks for local grunt
* user selects grunt plugins to install
* list standard plugins
* allow user to add custom plugins
* Gruntfile.js created with standard parameters
* package.json created with standard parameters
* project name is built with Joomla file infrastructure and files
* creates projectname manifest file with user data

### Modify User data
* Modify User data such as name, email etc

### Modify default Grunt parameters macro flow
* Modify settings for Grunt.
* lookup list of parameters
* select true/false
* file selection
* custom functions

### Modify Grunt Plugins parameters macro flow
* Modify settings for Grunt Plugins.
* select plugin name
* lookup list of parameters
* select true/false
* file selection

### Add other plugins macro flow
* Add user defined plugins to grunt list.
* Add name
* add url

### Help macro flow
* Local help file of how to use the builder.
* Option to add other help files.


## Joomla Project Macros
after project is created
### Modify plugin parameters
* options to modify parameters of plugins

### modify package.json
* modify package.json

### Build
* Build project

### Build and install
* Checks to see if project has been installed on Joomla Server
* Build and install project onto Joomla server

### FTP Config
* setup ftp configuration
* url
* port number
* login name
* password

### FTP Upload project
* select files to upload

### Run grunt on files
* run grunt default

### Run grunt plugins on files
* run selected grunt plugins

### Clean up
* clean up temp files

### Compress for deployment
* compress files to zip
* exclude non essential files list

## Other Functions

## Autocomplete functions
* user types in joomla specific code

* intelisense / autocomplete

* For example if label is added ie MYPROJECT.THISISDESCRIPTION the builder then adds label data and prompts user to add text to the language file.

* if JFACTORY:: is typed a popup will display options and insert dummy values


<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

  ga('create', 'UA-66284973-1', 'auto');
  ga('send', 'pageview');

</script>

