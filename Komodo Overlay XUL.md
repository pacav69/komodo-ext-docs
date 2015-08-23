# Files in root
## Conventions used
Anything within curly brackets {} including the {} is required to be replaced.

##root/content

### komodoOverlay.xul
contains list of menu selections

<code>

    <?xml version="1.0" encoding="utf-8" ?>

</code>

*  Location of language file used with xul 

<code>

    <!DOCTYPE overlay SYSTEM 			           "chrome://{extension_name}/locale/jphpextgen.dtd">

</code>

* location of stylesheets

<code>

    <?xml-stylesheet href="chrome://{extension_name}/skin/komodoOverlay.css" type="text/css" ?>
    <?xml-stylesheet href="chrome://{extension_name}/skin/hyperlink/cssImagePreview.css" type="text/css" ?>

</code>

* overlay id

<code>
    
    <overlay id="{extension_name}" xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">

</code>

* scripts used in xul

<code>
    
    <script type="application/x-javascript;version=1.7" src="chrome://komodo/content/library/encodingmenu.js" />
    <script type="application/x-javascript"             src="chrome://{extension_name}/content/{extension_nameExtProject.js" />
    <script type="application/x-javascript"             src="chrome://{extension_name}/content/scripts/statusbar.js" />

</code>

* menubar

<code>
    
    <menubar id="menubar_main">
    
</code>

* inserts menu after helpmenu

<code>
    
		<menu id="{MENuNAME}" label="{MENU_TITLE}" insertafter="helpMenu">
			<menupopup>
            
</code>
            
* first menu item about
        
<code>
    
	    <menuitem id="info" label="About {extension_name} Tools …"     oncommand="window.openDialog('chrome://{extension_name}/content/info/info.xul','Info','chrome,centerscreen,modal');"
                        class="menuitem-iconic" image="chrome://{extension_name}/content/skin/classic/images/information.png"/>
                    <menuseparator />
                    <menuitem id="create{extension_name}Project"
                            label="Create {extension_name} Extension Project"
                            oncommand="ko.{extension_name}.createExtGenProject('{projectbuild}');"
                            class="menuitem-iconic"/>
                    <menuseparator />
                    <menuitem id="modifyExtPrefs"
                            label="Modify {extension_name} Extension Prefs"
                            oncommand="window.openDialog('chrome://{extension_name}/content/pref/extprefs.xul','Info','chrome,centerscreen,modal');"
                            class="menuitem-iconic"/>
                    <menuseparator />
                </menupopup>
            </menu>
        </menubar>
    </overlay>
                 

</code>

*   draws a line on the menu list

<code>
    
    <menuseparator />
    
</code>
