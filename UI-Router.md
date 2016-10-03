## UI-Router

###Setup

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

***app.js***
* Same old app.js setup but now we add the "ui.router" into the array instead of leaving it blank. 
```
angular.model('uiRoutDemo', ['ui.router'])
```
