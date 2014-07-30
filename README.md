Remote MacOS Volume Controller
====
#### This service helps you controll the system volume of your MacOS with you smartphone, via the Internet. 

Design (not final)
--
### Tech
* System Architecture
 * Server
 * Client: 
   * Smartphone 
   * Mac
* Server Backend: 
 * Node.js
 * Host on Heroku

### Flow
1. User opens web page from her Mac's browser.
2. JS in web page detects that the page is served to a Mac. If so, load **mac.js**.
3. User logins to the service from Mac.
4. User opens web page from her phone.
5. JS in web page detects that the page is served to a Smartphone. If so, load phone.js.
6. User logins to the service from phone.
7. User sends volume controlling request from phone to server.
8. Server pushes the actions to be done to Firebase.
9. mac.js parses the actions to be done from Firebase instance, and forwards the final directives to AppleScript.
