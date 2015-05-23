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

#License

Copyright (c) 2015 Mridul Manas

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
