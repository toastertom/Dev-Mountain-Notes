## HTTP & Promises

A ***"promise"*** represents the eventual result of an asynchronous operation. It is a placeholder into which the successful result value or reason for failure will materialize.

* To make a promise in Angular you need to use ***$q***.

```
// To Make A Promise & Resolve It

angular.module('app').service('service1',function($q){

  this.getUnicorn = function (){

  //Step 1: Make the deferrer
    var deferrer = $q.defer();

  //Step 3: Resolve or Reject the promise
    deferrer.resolve('Sparkly Unicorn');
    deferrer.reject('Unicorns do not exist');

  //Step 2: Return the promise
    return deferrer.promise;
  }

  });
```
```
// Access the promise on the controller

angular.module('app').controller('controller', function($scope, service1){

  $scope.my6yearOldWantsAUnicorn = function() {
    var aPromise = service1.getUnicorn();
    aPromise.then(function(whateverDollaQResolved){
      $scope.theThingWeAskedFor = whateverDollaQResolved;
      })
  }

  });
```
