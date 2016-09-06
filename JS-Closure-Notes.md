# JS Closure Notes

##  Synchronous vs. Asynchronous
* Synchronous = In order. Meaning the computer will only execute one line of code at a time.
* Asynchronous = Not in Order. Meaning the computer can execute different lines of code at the same time. Not necessarily in order. JavaScript is asynchronous.

*  CallBacks are a function that is passed to another function as a parameter.
```
var friends = ["Mike", "Stacy", "Andy", "Rick"];
​
friends.forEach(function (eachName, index){
console.log(index + 1 + ". " + eachName); // 1. Mike, 2. Stacy, 3. Andy, 4. Rick​
});
```
* Constructor Pattern is a way of creating objects. Function below is used to create new objects.
```
var User = function(name) {
  this.name = name;
}

var bret = new User('Bret');
var tim = new User('Tim');
```
* Prototype
```
var Person = function(first, last) {
  this.first = first;
  this.last = last;
}

Person.prototype = {
  getName: function() {
    console.log(this.first + ' ' + this.last);
  }
}

new trump = new Person('Donald', 'Trump');
trump.getName();

var Student = function(first, last, grade) {
  this.first = first;
  this.last = last;
  this.grade = grade;
}

Student.prototype = Object.create(person.prototype);

var student = new Student('Bret', 'Little', 'B');
student.getName();
```
