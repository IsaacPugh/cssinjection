# CSS Injection

To inject CSS into a webpage, run this code in the console on your browser:
```javascript
var xmlHttp = new XMLHttpRequest();
xmlHttp.onreadystatechange = function() {
  if (xmlHttp.readyState == 4 && xmlHttp.status == 200) {
    var css = document.createElement('style');
    css.innerHTML = "\n" + xmlHttp.responseText + "\n";
    document.head.appendChild(css);
  };
};
xmlHttp.open( "GET", 'https://raw.githubusercontent.com/IsaacPugh/cssinjection/master/style.css', true );
xmlHttp.send( null );
```

Another good way to use this code is to use a
<a href="http://mrcoles.com/bookmarklet/"> bookmarklet generator</a> to create
a bookmarklet that you can click on to affect a webpage more easily.
