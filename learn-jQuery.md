# jQuery 官方资料学习笔记

> 学习中心 <http://learn.jquery.com/> 相当于官方的 tutorial
> API 查询 <http://api.jquery.com/> API 查询地点


## Using jQuery Core

### $ vs $()
 $ 返回的是 jQuery 函数 $() 返回的是 jQuery 对象


### 在 document 加载完成后，执行 script
```javascript
$( document ).ready(function() {
    console.log( "ready!" );
});
```


### conflicts  针对 $ 的冲突  两种解决方法，遇到了再查吧 不看了
* Attributes `.attr()` Method   both setter and getter

**setter**

```javascript
$( "a" ).attr( "href", "allMyHrefsAreTheSameNow.html" );

$( "a" ).attr({
    title: "all titles are the same too!",
    href: "somethingNew.html"
});
```
**getter**

```javascript
$( "a" ).attr( "href" );
// Returns the href for the first a element in the document
```
### Selecting Elements

* id
* class name
* attr
* compound CSS selector
* a Comma-separated List of Selectors
* Pseudo-Selectors
* Choosing Selectors 用对象的长度作为判断的依据，不然对象
```javascript
        // Testing whether a selection contains elements.
if ( $( "div.foo" ).length ) {
    ...
}
```
* Refining & Filtering Selections  微调  选择内容

```javascript
    // Refining selections.
$( "div.foo" ).has( "p" );         // div.foo elements that contain <p> tags
$( "h1" ).not( ".bar" );           // h1 elements that don't have a class of bar
$( "ul li" ).filter( ".current" ); // unordered list items with class of current
$( "ul li" ).first();              // just the first unordered list item
$( "ul li" ).eq( 5 );              // the sixth
```
### Working with Selections

* link Getters & Setters
* Chaining


### Getting and Setting Information About Elements

*  Getting and Setting Information About Elements

.html() – Get or set the HTML contents.
.text() – Get or set the text contents; HTML will be stripped.
.attr() – Get or set the value of the provided attribute.
.width() – Get or set the width in pixels of the first element in the selection as an integer.
.height() – Get or set the height in pixels of the first element in the selection as an integer.
.position() – Get an object with position information for the first element in the selection, relative to its first positioned ancestor. This is a getter only.
.val() – Get or set the value of form elements.
