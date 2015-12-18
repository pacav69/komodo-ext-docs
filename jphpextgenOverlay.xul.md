# Description of projectname overlay.xul
## files in root/content

## komodoOverlay.xul
contains list of menu selections


    <?xml version="1.0" encoding="utf-8" ?>
.
*  Location of language file used with xul

        <!DOCTYPE overlay SYSTEM "chrome://jphpext/locale/jphpextgen.dtd">
.
* location of stylesheets

        <?xml-stylesheet href="chrome://createjphpextproject/skin/komodoOverlay.css" type="text/css" ?>
        <?xml-stylesheet href="chrome://createjphpextproject/skin/hyperlink/cssImagePreview.css" type="text/css" ?>


* overlay id

        <overlay id="createjphpextproject" xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">


* scripts used in xul
    
        <script type="application/x-javascript;version=1.7" src="chrome://komodo/content/library/encodingmenu.js" />
        <script type="application/x-javascript"             src="chrome://jphpextgen/content/createJPHPExtProject.js" />
        <script type="application/x-javascript"             src="chrome://jphpextgen/content/scripts/statusbar.js" />


* menubar

        <menubar id="menubar_main">


* inserts menu after helpmenu

            <menu id="jphptools" label="JPHP Tools" insertafter="helpMenu">
                    <menupopup>
 
 
* first menu item about
    
                    <menuitem id="info" label="About JPHP Tools …"     oncommand="window.openDialog('chrome://jphpextgen/content/info/info.xul','Info','chrome,centerscreen,modal');"
                        class="menuitem-iconic" image="chrome://jphpextgen/content/skin/classic/images/information.png"/>
                    <menuseparator />
                    <menuitem id="createJPHPExtProject"
                            label="Create Joomla Extension Project"
                            oncommand="ko.jphpextgen.createExtGenProject('jphp');"
                            class="menuitem-iconic"/>
                    <menuseparator />
                    <menuitem id="modifyJPHPExtPrefs"
                            label="Modify Joomla Extension Prefs"
                            oncommand="window.openDialog('chrome://jphpextgen/content/pref/jextprefs.xul','Info','chrome,centerscreen,modal');"
                            class="menuitem-iconic"/>
                    <menuseparator />
                </menupopup>
            </menu>
        </menubar>
    </overlay>
 
 
 
*   draws a line on the menu list

        <menuseparator />

