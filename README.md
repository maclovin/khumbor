
# Khumbor (Thumbor url builder)

### Khumbor is a Thumbor client for Node JS powered by [Kanui](http://https://github.com/Kanui/QueroSerKanui)

_(A improved version of [https://github.com/PolicyMic/thumbor](https://github.com/PolicyMic/thumbor))_

### Usage after clone or install

```
var Khumbor = require('khumbor');

var thumbor = new Khumbor('[key]', 'http://thumbor.localhost.dev:8888');
var img = 'http://upload.wikimedia.org/wikipedia/en/a/ab/King_of_the_Beach_(Wavves)_album_cover.jpg';

// 3 different sizes of the same image, with the same instance. 
var thumborUrl = [
	thumbor.setImagePath(img).fitIn(355, 355).halign('center').buildUrl(),
	thumbor.setImagePath(img).fitIn(250).halign('center').buildUrl(),
	thumbor.setImagePath(img).fitIn(160).filter('fill(white)').buildUrl()
];
                                           
```
### Improvements

* Now you can set blank values to "Resize" and "Fitin" (100x or x100). 
* I decided to create a check on the filtersCalls push. In this way, we don't need to create another Thumbor instance to use the same filters with another image url.

### Contact

If u want to contribute, tell me something or give me a beer, pls mail me: [m4k2005@yahoo.com](m4k2005@yahoo.com).






_hail ⚕_