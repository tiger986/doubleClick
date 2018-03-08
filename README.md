## Double click elements do not trigger their click events
#### JS code
```javascript
var time = null;		
$('.d').click(function(){
    clearTimeout(time);
    time = setTimeout(function(){
	console.log("Single click");
    },300);
});
		
$('.d').dblclick(function(){
    clearTimeout(time);
    console.log("Double click");
});
