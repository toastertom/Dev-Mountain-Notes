# UI-Router

##Setup

###Step1
***HTML***
* Top of the Document (Same old stuff).
```
<!DOCTYPE html>
<html ng-app="uiRoutDemo">
```
* Add the new Angular-UI-Router script below your normal angularjs src. (This is new).
```
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.8/angular.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/angular-ui-router/0.3.1/angular-ui-router.min.js"></script>
```
---
###Step 2
***app.js***
* Same old app.js setup but now we add the "ui.router" into the array instead of leaving it blank. Anything in the array is considered a dependence for the app to function.  
```
angular.model('uiRoutDemo', ['ui.router'])
```
* Then you will you will use .config which will be used to configure what you want. 
```
angular.model('uiRoutDemo', ['ui.router'])

.config(function($urlRouterProvider, $stateProvider){

  });
```
---
###Step 3 (Last Step)
***HTML***
* Next you need to setup the point you want your content to be swapped out. Note do not put anything in the ui-view because it will be swapped out with other content.
```
<ui-view>
  <!-- Do not put anything here, it will be replaced. -->
</ui-view>
```
---
