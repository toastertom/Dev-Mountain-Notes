# UI-Router

##Setup

###Step1
***index.html***
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
***index.html***
* Next you need to setup the point you want your content to be swapped out. Note do not put anything in the ui-view because it will be swapped out with other content.
```
<ui-view>
  <!-- Do not put anything here, it will be replaced. -->
</ui-view>
```
---

## Using UI-Router

***app.js***
* follow the template below to build a simple template. Note "state" means more like status. What is the status of eg. home , profile , friendsList.
```
angular.model('uiRoutDemo', ['ui.router'])

.config(function($urlRouterProvider, $stateProvider){

  $stateProvider.state('home', {

    template: '<h3>You Are Home</h3>',
    url: '/home'
    })

  $stateProvider.state('profile', {

    template: '<h3>Your Profile Page</h3>',
    url: '/profile'
    })
  });
```
---

***app.js***
* We don't actually want to build templates in our app.js file. Instead have "template:" be "templateUrl:" with a link to a separate html file.
```
angular.model('uiRoutDemo', ['ui.router'])

.config(function($urlRouterProvider, $stateProvider){

  $stateProvider.state('home', {

    templateUrl: 'home-tmpl.html',
    url: '/home'
    })

  $stateProvider.state('profile', {

    templateUrl: 'profile-tmpl.html',
    url: '/profile'
    })
  });
```
---

***home-tmpl.html***
* Now under the home template you can just code. Note you don't need to do all the head and script linking stuff because technically this code is being inserted into the original index.html doc's body that already has all that.
```
<h3>You are home</h3>
```
---

***app.js***
* Another thing that we can do is add specific controllers to each page. See below.
```
angular.model('uiRoutDemo', ['ui.router'])

.config(function($urlRouterProvider, $stateProvider){

  $stateProvider.state('home', {

    templateUrl: 'home-tmpl.html',
    url: '/home',
    controller: 'home-controller.js'
    })

  $stateProvider.state('profile', {

    templateUrl: 'profile-tmpl.html',
    url: '/profile',
    controller: 'profile-controller.js'
    })
  });
```
---

***home-controller.js***
* So our $state that is "home" is now attached to this controller.
```
angular.module('uiRoutDemo')

.controller('home-controller', function($scope, service ,$state){

  $scope.linkList = [
      'profile',
      'friends',
      'hobbies'
  ];

  });
```
---

***home-tmpl.html***
* Where the template is attached to the controller we can now use the power of angular on a this template. We will have different controllers for different templates.... normally.
```
<h3>You are home</h3>
<ul>
  <li ng-repeat="link in linkList">
    {{link}}
  </li>
</ul>
```
---
