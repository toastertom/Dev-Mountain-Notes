### AngularJs Linking Pages

* First create the  ***app.js*** "Module". A module contains the different components of an AngularJS app. Then place the following code:

```
var app = angular.module("myApp", []);
```
Or just
```
angular.module('myApp', [])
```
---
* Then create your ***controller.js*** file, a controller manages the app's data. Insert the following code:

```
app.controller('MainController', ['$scope', function($scope){ }]);
```
Or
```
angular.module('myApp').controller('mainCtrl', function ($scope , services) {});
```
---
* Then create a ***service.js*** file, and put the following code:

```
????
```
Or
```
angular.module('myApp').service('services', function () {});
```
---
* Lastly we need to connect our angular files to our HTML page.

Start by:
```
<html ng-app="myApp">
```
***ng-app*** is known as a ***"Directive"***. It tells AngularJs that the myApp "Module" lives within the HTML's "Scope."


* Just like we did with the HTML Tag we are going to put ng-controller  in the Body Tag:

```
<body ng-controller="MainController">
```
ng-controller is a "Directive" that defines the controller scope. In this case it would be anything within the Body Tags.
---
