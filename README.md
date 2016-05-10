NPM-module for Pushwoosh Web Push SDK  
=========================  
##Integration

**1.** Install npm-module  

**2.** Create a manifest.json file with the JSON content below, and place it in the root directory of your website:   

```javascript
{  
  "name": "Pushwoosh Demo",  
  "short_name": "Pushwoosh Demo",  
  "display": "standalone",  
  "gcm_sender_id": "123456789012", // Your GCM Project Number
  "gcm_user_visible_only": true 
}
```
**3.** Copy `service-worker.js` file from module to you project static folder.  

**4.** Add your Pushwoosh Application Code, default icon path, default title and service-worker path in `service-worker.js`     

**5.** Require and call module with params: *serviceWorkerURL, safariPushID, appCode*
```javascript
var push_notification = require('pushwoosh-notification');
push_notification('/service-worker.js','web.com.pushwoosh.websiteid','XXXXX-XXXXX');
```


=========================  

Safari push notifications:  
http://docs.pushwoosh.com/docs/safari-website-notifications  

Google Chrome guide (Available from version 42 of Google Chrome browser):  
http://docs.pushwoosh.com/docs/chrome-web-push  
http://docs.pushwoosh.com/docs/chrome-web-push-for-http-websites

Guide for Firefox push (Available from version 44 of Mozilla Firefox):  
http://docs.pushwoosh.com/docs/firefox-web-push

