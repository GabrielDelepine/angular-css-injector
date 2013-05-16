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

1. First, add the module "" to your AngularJS apps

     angular.module('myModule', ['DynamicStylesheets']);


2. Get this service where you want and add your css files in your HTML page ! Example here in a controller :

     function MyCtrl($scope, dynamicStylesheets)
     {
         dynamicStylesheets.add("/path/to/your/css/file.css");
     }
