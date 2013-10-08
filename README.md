angularDynamicStylesheets
=========================

A angularJS service to load dynamically CSS files

=====
Description
====
angularDynamicStylesheets is a AngularJS service allows you to load dynamically CSS files in your HTML page.

====
How to use ?
====

1. First, add the module "DynamicStylesheets" to your AngularJS apps

     angular.module('yourModule', ['DynamicStylesheets']);


2. Get this service where you want and add your css files in your HTML page ! Example here in a controller :

     function MyCtrl($scope, dynamicStylesheets)
     {
         dynamicStylesheets.add("/path/to/your/css/file.css");
     }

3. To remove all added CSS files when the page change (in a single page application), set the single page mode :
     function MyCtrl($scope, dynamicStylesheets)
     {
         dynamicStylesheets.setSinglePageMode(true);
     }

4. To remove manually all added CSS files, call the function removeAll :
     function MyCtrl($scope, dynamicStylesheets)
     {
         dynamicStylesheets.removeAll();
     }

====
Compatibility
====
IE >= 8

FF >= 3.5

Chrome >= 4

Opera >= 10


To make it IE7 compatible, delete "queryselector" in the code but you will need to include jQuery in your page.
About "queryselector" compatibility : http://caniuse.com/queryselector

====
Dependencies
====
No one (only angular of course).

Code tested with angular 1.0.8

