# line-notify
A demo server to send messages through LINE notify 

### Setup on OpenShift
 - You need to have an [OpenShift](https://www.openshift.com/) account first. 
 - Login to OpenShift Web management console 
 - Create an cartridge for the latest Node.js and `git clone` this project to your cartridge
 - After the process, OpenShift will do the rest things.

### Setup on LINE Notify 
 - Create a new [LINE notify](https://notify-bot.line.me/my/services/new) 
 - Fill in the required information
 - Make sure your Callback URL is: https://[your-cartridge].rhcloud.com/add-notify-user
 - Get your `CHANNEL_TOKEN` from web console and paste it to the file `line-notify.js` 

### Setup on your LINE
 - First, login your LINE on PC/mobile
 - Acceess `https://[your-cartridge].rhcloud.com/oauth.html` by the browser
 - Click `connect` to create an OAuth2 connection between LINE Notify and your cartridge, then your server is alllow to send notifications. 
 - Send test messages by: `curl -X GET https://[your-cartridge].rhcloud.com/line-notify` 

### Reference
 - [LINE Notify](https://notify-bot.line.me/en/)
 - [LINE Notify API](https://notify-bot.line.me/doc/en/)

### Demo
 ![demo](https://github.com/calmelated/line-notify/blob/master/line-notify.jpg?raw=true)
 
