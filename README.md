ngScrollTo
==========

Simple AngularJS scroll-to directive

fiddle : http://jsfiddle.net/8Mtxc/

``` html
<div ng-app="myApp">
 <p>Top</p>
 <div>
   <a scroll-to="section1">Goto Section 1</a>
 </div>
 <div style="padding-top:1000px">...</div>
 <div id="section1">
  <h2>Section1</h2>
  <a scroll-to="">Back to Top</a>
 </div>
</div>
```

``` javascript
angular.module("myApp", ["ngScrollTo"]);
```
