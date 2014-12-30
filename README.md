ngScrollTo
==========

Simple AngularJS scroll-to directive

fiddle : [http://jsfiddle.net/8Mtxc/86/](http://jsfiddle.net/8Mtxc/86/)

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


##Usage
###Default

``` javascript
angular.module("myApp", ["ngScrollTo"]);
```
###Custom action
Example: [http://jsfiddle.net/8Mtxc/85/](http://jsfiddle.net/8Mtxc/85/)
``` javascript

angular.module("myApp", ["ngScrollTo"])
.config(function(ngScrollToOptionsProvider) {
    ngScrollToOptionsProvider.extend({
        handler: function(el) {
          $(el).scrollintoview();
        }
    });
});

```
Update 0.0.5
* Added ngScrollToOptions provider.
* Made scrollIntoView to be replaceable by a custom function.

Update 0.0.4
* Added ScrollTo service for programatically scrolling.

Update 0.0.3
* Added optional offset attribute. The optional offset attribute allows scrolling an element into view and offset it by a specified number of pixels.

Update 0.0.2
* Made scrolling-to-top gets detected before searching for the target DOM element. (This change makes broken scroll-to link to be ignored instead of scrolling to top)
* Removed unnecessary $parse dependency.
