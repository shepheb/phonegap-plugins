# ExtractZipFile Phonegap Plugin for iOS #
by Shaun Rowe

This plugin allows you to extract a zip file

## Adding the Plugin to your project ##

To install the plugin, copy ZipPlugin.js to your project's www folder and include a reference to it in your html files.

<script type="text/javascript" src="ZipPlugin.js"></script>

Add SSZipArchive directory, ExtractZipFilePlugin.h and ExtractZipFilePlugin.m to the Plugins directory of your phonegap project.

Add a plugin line to your cordova.plist
ExtractZipFilePlugin - String - ExtractZipFilePlugin

## Using the plugin ##

    function extractFile(fileName)
    {
        window.plugins.extractZipFile.extractFile(fileName,destination,win,fail);
    }

    function win(status) 
    {	 
        alert('Success'+status);
    }	 
  
    function fail(error) 
    { 
        alert(error);
    }

## Function Call ##

<input type="button" value="Extract Zip File" onClick="extractFile('/path/to/ZipFile.zip');"/>