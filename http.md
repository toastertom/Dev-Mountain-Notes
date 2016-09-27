## HTTP Notes & JSON

---

***REST***: Is an internet protocol for sending and receiving data.
* ***GET***: Is to retrieve data from a server.
* ***PUT***: Is to update and existing object on the server.
* ***POST***: Is to create a new object on the server.
* ***DELETE***: Deletes the information from the server.

---

***$http Syntax***
```
$http.get('https://AnyURLGoesHere.com/api/dogs')
  .then(function(dogs){
    var status = dogs.status;
    var data = dogs.data;
    })
```
Whatever is returned from an http call is know as an ***Promise***.

---

######Promise Definition
A ***promise*** represents the eventual result of an asynchronous operation. It is a placeholder into which the successful result value or reason for failure will materialize.

---
