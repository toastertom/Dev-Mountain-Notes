## HTTP & Promises

A ***"promise"*** represents the eventual result of an asynchronous operation. It is a placeholder into which the successful result value or reason for failure will materialize.

* To make a promise in Angular you need to use ***$q***.

```
// To Make A Promise & Resolve It

angular.module('app').service('service1',function($q){

  this.getUnicorn = function (){
    var deferrer = $q.defer();

    deferrer.resolve('Sparkly Unicorn');

    return deferrer.promise;
  }

  });
```
