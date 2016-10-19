#Custom Directives with Angular

***Directive:*** AngularJS directives are extended HTML attributes with the prefix ng-.

---
###Step 1
***custDirec.js***
* Create a js file for your directive and fill in the following.
```
angular-model('nameOfApp').directive('custDirecName', function(){
  return {
    template: 'customdirectiveName.html'
  }
  });
```
---
###Step 2
***Html***
* Then you need to link your custom directive file to your html file and specify where the template will show up. Note that html doesn't like camel case so angular converts the name of your custom directive to snake case (eg. word-word).
```
<name-of-app></name-of-app>

<script src="./custom-directive.js"></script>
```
---
