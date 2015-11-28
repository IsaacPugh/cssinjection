# CSS Injection

To run this, run:
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
