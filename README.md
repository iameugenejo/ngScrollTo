ngScrollTo
==========

Simple AngularJS scroll-to directive

``` html
<div ng-app="app">
 <p>Top</p>
 <div ng-controller="myCtrl">
   <a scroll-to="section1">Section 1</a>
 </div>
 <div style="padding-top:1000px">...</div>
 <div id="section1">
  <h2>Section1</h2>
  <a scroll-to="">Back to Top</a>
 </div>
</div>
//
```
