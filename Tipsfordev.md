# Tips for development

## prefs.xml 

If using code to modify prefs.xml file make a back up before proceding

location on a mac
/Users/{username}/Library/Application Support/{KomodoIDE}|{KomodoEDIT}/{Version number}

e.g.
/Users/admin/Library/Application Support/KomodoIDE/9.2

// TODO: locations on linux windows

## extensions installes location
/Users/silvermac/Library/Application Support/KomodoIDE/9.2/XRE/extensions


Where does Komodo keep settings data?

Komodo stores preferences, macros, templates, keybinding schemes and other settings in a user-specific directory called the user data directory. The name and location of this directory varies depending on the operating system and Komodo version:

Windows Vista, Windows 7, Windows 8 or newer
C:\Users\<user>\AppData\Local\ActiveState\Komodo[IDE|Edit]\<version>
Windows XP or older
C:\Documents and Settings\<username>\Local Settings\Application Data\ActiveState\Komodo[IDE|Edit]\<version>
Linux
/home/<user>/.komodo[ide|edit]/<version>
Mac OS X
/Users/<user>/Library/Application Support/Komodo[IDE|Edit]/<version>
