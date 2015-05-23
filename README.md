# ImgResize.JS
A Simple JavaScript Function to resize Image after getting the Window size.

## What does ImgResize.JS do?
ImgResize.JS is a simple JS Function which gets the browser width and height and changes the image height and width accordingly. This also works when the user resizes browser window or when the website is displayed in mobile browsers.

## Usage
ImgResize.JS is easy to use with no hassle.It uses ``` window.innerWidth ``` and ``` window.innerHeight ``` to get the width of the window even when the browser window is resized. 

### Get Window Size and give it out through ``` alert ```

The following code gets the Browser height and window through ``` var height = window.innerHeight || $(window).height();```
and ``` var width = window.innerWidth || $(window).width();```
The Height and Width values received are then given out through ``` alert ``` .
```
<script>
var TO = false;
    var resizeEvent = 'onorientationchange' in window ? 'orientationchange' : 'resize';
    $(window).bind(resizeEvent, function() {
        TO && clearTimeout(TO);
        TO = setTimeout(resizeBody, 200);
    });
    function GetHeightWidth(){
        var height = window.innerHeight || $(window).height();
        var width = window.innerWidth || $(window).width();
        alert(height);
        alert(width);
    }
 </script>
 
  ```
### Change Image Size with Height and Width values received 
  The following code gets the Browser height and window through ``` var height = window.innerHeight || $(window).height();```
and ``` var width = window.innerWidth || $(window).width();```

Another function changes the Image size using the values received.
```
<script>
     function resizeImg(){
     document.getElementById("art1").width = window.innerWidth || $(window).width();

   }
</script>
```

## Calling Function through ``` onload ```

Use both functions by calling functions in chains: ``` <body onload="GetHeightWidth(); ImgResize();"> ```
