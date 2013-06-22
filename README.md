ngScrollTo
==========

Simple AngularJS scroll-to directive

fiddle : http://jsfiddle.net/8Mtxc/1/

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

Update 0.0.2
* Made scrolling-to-top gets detected before searching for the target DOM element. (This change makes broken scroll-to link to be ignored instead of scrolling to top)
* Removed unnecessary $parse dependency
