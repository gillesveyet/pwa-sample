# PwaSample

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.4.

PWA support according to: https://angular.io/guide/service-worker-getting-started

Add To Home Screen: https://stackoverflow.com/questions/53871586/angular-catch-beforeinstallprompt-event-add-to-homescreen-in-dev-tools-applic  
May no longer be necessary with Chrome 75+ : https://techdows.com/2019/03/install-pwas-from-omnibox-chrome.html

## Build for deployment

Designed to be deployed on `/pwa-sample` path.  
Check https://gillesveyet.yo.fr/pwa-sample/

Build command: `ng build --prod --base-href /pwa-sample/`

Path was manually added to src/manifest.json:
```json  
"scope": "/pwa-sample/",
"start_url": "/pwa-sample/",
```

## Test with local server

Edit src/manifest.json to remove `/pwa-sample`
```json  
"scope": "/",
"start_url": "/",
```

Run `ng build --prod`  
Launch local server:  `http-server -c-1 dist/pwa-sample`  
Open browser on `http://127.0.0.1:8080`
