[[_TOC_]]

# Introduction
When creating an extension you need to have a specific goal in mind and work towards that goal.

# Tutorial for Komodo Extension
[Description of project files](Descriptionofprojectfiles)

After reading the instructions on [how to generate an extension](http://docs.komodoide.com/Manual/CreatingaKomodoExtension) we can proceed to create an extension.

# Create an extension
Create a project and use the name 'jbuilder'
After creating the project use the macro 'build and install'
This will display the Add-ons manager window.

![](http://i.imgur.com/sOwcSg3.png)
## Description of Add-ons manager
1. This project name and version number.
2. The icon of the extension.
3. The description of the project.
4. Information on the progress of the installed extension. 

After installing the extension you will be prompted to restart Komodo in order for the changes to take effect.

## Adding an about page
Our first goal is to create an about page


## Adding to menus
First open up 'jbuilder_extension_overlay.xul' located in the content directory and change the content between the menubar tags to read as follows: 

     <?xml version="1.0"?>
    <!DOCTYPE overlay PUBLIC "-//MOZILLA//DTD XUL V1.0//EN" "http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
    
    <overlay id="jbuilder_extension_Overlay"
     xmlns:html="http://www.w3.org/1999/xhtml"
     xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
     xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
    
    <!-- <menu id is a unique name -->
    
    	<menubar id="menubar_main">
    		<menu id="jbtools" label="JTools" insertafter="Tools">
    			<menupopup>
    				<menuitem id="info" label="About Joomla Tools …"
    						oncommand="window.openDialog('chrome://jbuilder_extension/content/info/info.xul','Info','chrome,centerscreen,modal');"
    class="menuitem-iconic" image="chrome://jbuilder_extension/skin/images/icon-information.png"/>
    			</menupopup>
    		</menu>
    	</menubar>
    
    </overlay>

Next you need to add the info.xul file
Create a directory named 'info' under the content directory then create a new file name 'info.xul'

add the following content info.xul
    
    <?xml version="1.0"?>
    <?xml-stylesheet href="chrome://global/skin/"?>
    <?xml-stylesheet href="chrome://jbuilder_extension/content/info/info.css" type="text/css"?>
    
    <?xul-overlay href="chrome://jbuilder_extension/content/info/about.xul"?>
    
    <?xml-stylesheet type="text/css" href="data:text/css,
    
    " ?><dialog id="info"
    	xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul"
    	xmlns:html="http://www.w3.org/1999/xhtml"
    title="About Joomla Tools"
    buttons="accept"
    onload="initInfo();">
    
    	<html:h1>Joomla Tools</html:h1>
    	<tabbox id="tablist">
    		<tabs id="info-tabs"/>
    		<tabpanels id="info-panels"/>
    	</tabbox>
    
    	<script>//<![CDATA[
    		var ko=window.opener.ko;
    		function initInfo() {
    			var i,l;
    			var links=document.getElementsByClassName('link');
    			for(i=0,l=links.length;i<l;i++) links[i].onclick=openUrl;
    		}
    		function openUrl() {
    			ko.browse.openUrlInDefaultBrowser(this.textContent);
    		}
    	//]]></script>
    
    
    </dialog>
    
    
create a new file and name it 'about.xul'

Add this content
    
    <?xml version="1.0"?>
    
    <overlay id="singleItemEx"
     xmlns:html="http://www.w3.org/1999/xhtml"
     xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
    		<tabs id="info-tabs">
    			<tab label="About"/>
    		</tabs>
    
    		<tabpanels id="info-panels">
    			<tabpanel id="about">
    				<html:div>
    					<html:p><html:strong>Version</html:strong> 0.0.1<html:br/>Copyright © Paul Cavanagh</html:p>
    
    					<html:p>
    						This Addon for Komodo Edit/IDE developers.<html:br/>
    						Second line of text <html:br/>
    					</html:p>
    					<html:p>some other text<html:br/>
    					</html:p>
    
    				</html:div>
    			</tabpanel>
    		</tabpanels>
    </overlay>
    
    
create a new file and name it 'info.css'
Add this content

    @namespace html url("http://www.w3.org/1999/xhtml");
    	h1 {
    		font-size: 18px;
    	}
    	h2 {
    		font-size: 12px;
    	}
    	h3 {
    		font-size: 10px;
    	}
    	p {
    		margin: 0px 0px 8px 0px;
    	}
    	th, td {
    		text-align: left;
    		vertical-align: top;
    	}
    	span.button {
    		font-weight: bold;
    		padding: 2px 4px;
    		border: 1px solid #B1B1B1;
    		box-shadow: inset -1px 1px 1px #EEEEEE;
    		border-radius: 2px 2px 2px 2px;
    		background-color: white;
    		background: linear-gradient(to bottom,#DDDDDD,#BDBDBD);
    	}
    	span.link {
    		font-weight: bold;
    		padding: 2px 4px;
    		border: 1px rgb(128,128,128);
    		border-style: none none dotted none;
    		background-color: white;
    	}
    
    	tabpanels#info-panels>tabpanel>table {
    		float: left;
    	}
    
Under the root directory create a directory named 'skin' then create a sub directory name it 'images'
add an image file of 32*32 pixels name it 'icon-information.png'

The directory structure will look like this
    
    
    ├───build
    │   ├───jar
    │   │   └───content
    │   └───xpi
    ├───content
    │   └───jbuilder_extension_overlay.xul
    │   └───info
    │   	└───info.xul
    │   	└───about.xul
    │   	└───info.css
    └───skin
    	└───images
    		└───icon-information.png
    
Save all files
Run the 'build and install'

Then a new menu will appear

![](http://i.imgur.com/KIMdx1C.png)


## Menu separator
A menu separator will draw a line between menu items
Just place the following code after the menuitem closing tag and before the next menuitem.
 
	<menuseparator />

## Icons
For an icon to appear in the add-ons manager you need to add the iconURL tag to the install.rdf file like below and place the icon in the skin/images directory.
The best size is 48*48 pixels.

        <em:homepageURL>http://silverpcgroup.com/jbuilder_extension</em:homepageURL>
		<em:iconURL>chrome://jbuilder_extension/skin/images/Hammericon48.png</em:iconURL>

## Language files

## Style Sheets

## Overlay files

## Testing your extension

## Publishing your extension
http://komodoide.com/packages/submit-instructions/#pane-packages

