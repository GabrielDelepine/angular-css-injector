=====
Compatibility
====
The code was tested with angular 1.4.x

Angular-css-injector
=========================

A angularJS service to load dynamically CSS files. The original name of this project was angularDynamicStylesheets.

=====
Description
====
angular-css-injector is a AngularJS service allows you to load dynamically CSS files in your HTML page.

====
How to use ?
====

1. Your angular's app must be defined on the HTML tag of your page

```html
<html ng-app="myApp"
```
2. Add the module "angular.css.injector" to your AngularJS apps
```javascript
     angular.module('myApp', ['angular.css.injector']);
```

3. Get this service where you want and add your css files in your HTML page ! Example here in a controller :
```javascript
     function MyCtrl($scope, cssInjector)
     {
         cssInjector.add("/path/to/your/css/file.css");
     }
```
4. To remove all added CSS files when the page change (in a single page application), configure the `cssInjectorProvider`:
```javascript
	 myApp.config(function(cssInjectorProvider){
	 	 cssInjectorProvider.setSinglePageMode(true);
	 });
```

5. To remove manually all added CSS files, call the function removeAll :
```javascript
     function MyCtrl($scope, cssInjector)
     {
         cssInjector.removeAll();
     }
```

====
Compatibility
====
IE >= 8

FF >= 3.5

Chrome >= 4

Opera >= 10

====
Dependencies
====
No one (only angular of course).

Code tested with angular 1.2.14

====
Previous version
====
The module and the service name changed name from v1.0
Be careful and update your code if you use a previous version < 1.0
