# GTmetrix-Extension
Chrome Extension development example. In this tutorial we will be creating a simple chrome extension that will use GTmetrix to check the site speed of whatever site you happened to be browsing. 

What is a Chrome Extension?
A Chrome extension is just some HTML, CSS and JavaScript that allows you to add some functionality to Chrome through some of the JavaScript APIs Chrome exposes. An extension is basically just a web page that is hosted within Chrome and can access some additional APIs.

Getting started
  - Clone the whole repository on your computer.

Directory Structure:
  - icon.png: Default icon for your extension
  - manifest.json: It is a simple json file describing your extension. Most of the object in the file is self explanatory. 
    - If you look carefully you will see a "browser_action" section where we specify what the default icon is and what HTML page should be displayed when the Browser Action button is clicked
    - "permissions" section that specifies that we need to have permission to access the activeTab
  - popup.html: Contains the default UI of the extension. Here I have added only a simple button that will check the speed of the current site. Also, I have included a "popup.js" script that will have the required logic for the extension.
  - popup.js: This is the backend of the extension. Here I have attached an action listener to the button, that will get activated on click. When activated, the script creates a form that sends request to the "gtmetrix.com" and fetches result for the current tab.

Icon made by Popcorns Arts from www.flaticon.com 
Reference: https://www.sitepoint.com/create-chrome-extension-10-minutes-flat/
