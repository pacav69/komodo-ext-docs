# root/content

## komodoOverlay.xul
contains list of menu selections

<code>

    <?xml version="1.0" encoding="utf-8" ?>

</code>

*  Location of language file used with xul 

<code>

    <!DOCTYPE overlay SYSTEM "chrome://jphpext/locale/jphpextgen.dtd">

</code>

* location of stylesheets

<code>

    <?xml-stylesheet href="chrome://createjphpextproject/skin/komodoOverlay.css" type="text/css" ?>
    <?xml-stylesheet href="chrome://createjphpextproject/skin/hyperlink/cssImagePreview.css" type="text/css" ?>

</code>

* overlay id

<code>
    
    <overlay id="createjphpextproject" xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">

</code>

* scripts used in xul

<code>
    
    <script type="application/x-javascript;version=1.7" src="chrome://komodo/content/library/encodingmenu.js" />
    <script type="application/x-javascript"             src="chrome://jphpextgen/content/createJPHPExtProject.js" />
    <script type="application/x-javascript"             src="chrome://jphpextgen/content/scripts/statusbar.js" />

</code>

* menubar

<code>
    
    <menubar id="menubar_main">
    
</code>

* inserts menu after helpmenu

<code>
    
		<menu id="jphptools" label="JPHP Tools" insertafter="helpMenu">
			<menupopup>
            
</code>
            
* first menu item about
        
<code>
    
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
                 

</code>

*   draws a line on the menu list

<code>
    
    <menuseparator />
    
</code>
