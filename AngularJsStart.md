### AngularJs Linking Pages

First create your ***app.js*** folder. Then place the following code:

```
var app = angular.module("myApp", []);
```
Or just
```
angular.module('myApp', [])
```

Then create your ***controller.js*** file, and put the following code:

```
app.controller('MainController', ['$scope', function($scope){ }]);
```
Or
```
angular.module('myApp').controller('mainCtrl', function ($scope , services) {});
```
Then create a ***service.js*** file, and put the following code:

```
????
```
Or
```
angular.module('myApp').service('services', function () {});
```
Lastly we need to connect our angular files to our HTML page.

Start by:
```
<html ng-app="myApp">
```
***ng-app*** is known as a ***"Directive"***. It tells AngularJs that the myApp "Module" lives within the HTML's "Scope."
