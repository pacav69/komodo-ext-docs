## Installation ##
WIP

## Download and install Komodo IDE##

Download and install Komodo IDE

## Create a project ##

Open up Komodo and create a project in your installed MAMP

located on a MAC &apos;/applications/joomla-3.4.3-1/apps/joomla&apos; this will display all files in the left side panel of the IDE.

This will allow you to directly edit and debug your code.

## Configure IDE for debugging ##

### Modifying the php.ini file###

In order to use the debugger you need to modify the php.ini file of the Apache server you are using.
Follow these instructions

![Setup for debugging](https://github.com/pacav69/komodo-ext-docs/blob/master/img/komododebbugingsetup.png)

On a MAC using MAMP
* Goto /applications/joomla-3.4.3-1/php/etc/php.ini
* open up this file with your favourite text editor
* do a search for xdebug you should find something like this:

        ;[XDebug]
        ;; Only Zend OR (!) XDebug
        ;zend_extension=&quot;/Applications/mampstack-5.5.27-0/php/lib/php/extensions/xdebug.so&quot;
        ;xdebug.remote_enable=true
        ;xdebug.remote_host=127.0.0.1
        ;xdebug.remote_port=9000
        ;xdebug.remote_handler=dbgp
        ;xdebug.profiler_enable=1
        ;xdebug.profiler_output_dir=/tmp

Delete the ; in front of the text under &apos;;; Only Zend OR (!) XDebug&apos; so it reads like this:

        ;[XDebug]
        ;; Only Zend OR (!) XDebug
        zend_extension=&quot;/Applications/mampstack-5.5.27-0/php/lib/php/extensions/xdebug.so&quot;
        xdebug.remote_enable=true
        xdebug.remote_host=127.0.0.1
        xdebug.remote_port=9000
        xdebug.remote_handler=dbgp
        xdebug.profiler_enable=1
        xdebug.profiler_output_dir=/tmp


Then do a search for implicit_flush you will find

        implicit_flush = Off


Change the Off to On

        implicit_flush = On

Save your changes

Restart your apache server

###In the IDE###
Open up preferences select--&gt; languages --&gt;PHP

####Default php interpreter####
<img src="img/Komododebbugingsetup.png" alt="" width="400" height="508">

Under the label &apos;&apos;&apos;&apos;Default php interpreter&apos;&apos;&apos;&apos; use the following:
* goto &apos;&apos;&apos;&apos;Use this interpreter&apos;&apos;&apos;&apos; browse to
 /applications/joomla-3.4.3-1/php/bin/php

* Under the label &apos;&apos;&apos;&apos;Default composer interpreter&apos;&apos;&apos;&apos; browse to
 /applications/joomla-3.4.3-1/php/bin/php 

* Under the label &apos;&apos;&apos;&apos;Path to alternative PHP configuration file&apos;&apos;&apos;&apos; browse to
 /applications/joomla-3.4.3-1/php/etc/php.ini

####Listen for debugging####
Then select in preferences --&gt;Debugger--&gt;Connection

<h4>Debugger Connection<h4>

![Setup for debugging](https://github.com/pacav69/komodo-ext-docs/img/Komododebuggingconnection.png|)

Under &apos;&apos;&apos;&apos;Komodo should listen for debugging connections on:&apos;&apos;&apos;&apos; 
Change option to &apos;a specific port:9000&apos;
make sure it is set to 9000 this is what should be set in the php.ini file.

Open up preferences select--&gt; languages --&gt;PHP
Under the debugger Configuration you should see &apos;&apos;&apos;&apos;Successfully configured for local PHP debugging.&apos;&apos;&apos;&apos; If not you can click on &apos;Re-check Config&apos;

Click OK to save changes

<h4>Debugging options<h4>
![Setup for debugging](https://github.com/pacav69/komodo-ext-docs/img/KomodoDebuggingoptions.png|)

Under the debug menu select &apos;Step In&apos; this will open up a new window titled &apos;&apos;&apos;&apos;Debugging Options&apos;&apos;&apos;&apos;.
Create a new configuration name it &apos;&apos;&apos;&apos;joomlaphp&apos;&apos;&apos;&apos; click ok

* In &apos;&apos;&apos;Language&apos;&apos;&apos; enter in PHP

* In &apos;&apos;&apos;Interpreter Arguments&apos;&apos;&apos; click on the arrow to the right of the area 
select &apos;&apos;&apos;&apos;look for php.ini file in this directory&apos;&apos;&apos;&apos;.
browse to /Applications/joomla-3.4.3-1/php/etc
it will then display &apos;-c /Applications/joomla-3.4.3-1/php/etc&apos;

* In &apos;&apos;&apos;Script&apos;&apos;&apos; browse to 
/Applications/joomla-3.4.3-1/apps/joomla/htdocs/index.php

* In &apos;&apos;&apos;Directory&apos;&apos;&apos; browse to 
/Applications/joomla-3.4.3-1/apps/joomla/htdocs

Under the label &apos;&apos;&apos;&apos;Select the interpreter to use for debugging select option&apos;&apos;&apos;&apos; - &apos;&apos;&apos;&apos;Use the CGI interpreter (php-cgi or php)&apos;&apos;&apos;&apos;.

When ok is click it will start to run and open up the index.php and stop at the first entry point.
From there you can go/continue, step in, step over, and step out.

If go/continue is selected it will goto the first breakpoint in your code if you have created one.

