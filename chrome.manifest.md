root
## chrome.manifest

* content alias using extension name (jphpextgen) as reference

content jphpextgen jar:jphpextgen.jar!/content/

* skin alias

skin jphpextgen classic/1.0 jar:jphpextgen.jar!/skin/

* locale alias

locale jphpextgen en-US jar:jphpextgen.jar!/locale/en-US/


* overlay files

overlay chrome://komodo/content/komodo.xul chrome://jphpextgen/content/jphpextgen_overlay.xul
overlay chrome://komodo/content/pref/pref-jphp.xul  chrome://jphpextgen/content/pref/pref-jphpOverlay.xul
