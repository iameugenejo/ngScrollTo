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

Its also possible to use ScrollTo service directly.


``` javascript
ScrollTo.idOrName('section1');
```

Just add dependency to your application.


``` javascript
angular.module("myApp", ["ngScrollTo"]);
```

Update 0.0.4
* Added ScrollTo service for programatically scrolling.

Update 0.0.3
* Added optional offset attribute. The optional offset attribute allows scrolling an element into view and offset it by a specified number of pixels.

Update 0.0.2
* Made scrolling-to-top gets detected before searching for the target DOM element. (This change makes broken scroll-to link to be ignored instead of scrolling to top)
* Removed unnecessary $parse dependency
