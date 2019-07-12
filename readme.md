# TNT Videos ver1.3
Jquery code for TNT banners and optimized youtube videos with lazyload.

#### v 1.3
- SWAP for vimeo-solo option with data-mode="swap"
- Update/fix button's logic statements

#### v 1.2
- Small update for static banners, use data-mode="static" to vimeo players
- New responsive play append for mobile, use data-mobile-append-play="" 

#### v 1.1
- NEW Close button string option
- Fixed duplicate buttons
- Responsive Vimeo Solo, must include .thumbnail 

#### Known Issues
- Vimeo profile IDs, currently set to one profile ID
- Turn off animations on responsive.

## Dependents
- Get Device 
- Retrieve Youtube
- Fluid-vid

### Basic 
```javascript
$(function () {			
	$("[data-player]").tntvideos();	
});
```

### Basic Options 
```javascript
$(function () {			
	//tnvideos defaults
	$("[data-player]").tntvideos({		
		playButton: '.play',
		closeButton: '.close',
		bodyPlaying: '.playing',
		mobileWidth: 900
	});			
});
```

### Advanced Options
```javascript
$(function () {			
	//defaults
	$("[data-player]").tntvideos({		
		playButton: '.play',
		closeButton: '.close',
		closeButtonString: '<span><i class="icon-plus"></i></span>',
		bodyPlaying: null,
		animate: true,
		mobileWidth: 900,
		onPlay: function() {
			//do something
		},
		onClose: function() {
			//do something
		}
	});			
});
```

## Available Options
|  Defaults | Description  |
| ------------ | ------------ |
| playButton: '.play'  | Default class for the play button  |
| closeButton: '.close' |  Default class for the close button |
| closeButtonString: '<i class="icon-plus"></i> Close Video' | Default HTML string for the close button.
| animate: true  | Scroll animation to the top of the container  |
| bodyPlaying: null | Add a body playing class |
| mobileWIdth: 900 | Responsive width |
| mobileAppendPlay: null | Responsive attach play button |
| offset: Int | By default the offset is the height of the header, you can also use an integer.  |
| onPlay: function() | Callback function for the play button  |
| onClose: function() | Callback function for the close button |

## Video Items Data Options
|  Defaults | Description  |
| ------------ | ------------ |
| data-mode="static" | Use this with vimeo players for static banners  |
| data-mobile-append-play="[data-embed]" | Option to attach the play button on responsive.  |

## Banner Vimeo width Youtube Player(Normal) HTML
Default mode player shows a vimeo preview and on play renders a youtube video(thumbnail is genereated or can be custom)
```html
    <div class="banner" data-player="vimeo" data-vimeo="290738166.hd.mp4?s=ee27ae407692d8723a18b6c5e43356c7caac01a6">
    	<div data-embed="yEkWVQywXIE" data-width="560" data-height="315">
    		<img alt="youtube thumbnail" class="thumbnail" src="https://img.youtube.com/vi/yEkWVQywXIE/maxresdefault.jpg">
    	</div>
    	<div class="caption">
    		<h1>example caption</h1>
    		<a class="play">Play Video</a>
    	</div>
    </div>
```
    
## Banner Vimeo Solo Player HTML
For legacy banners banner previews a full vimeo video, on play the same vimeo video plays. (must have thumbnail image for responsive)
```html
    <div class="banner" data-player="vimeo-solo" data-vimeo="290738166.hd.mp4?s=ee27ae407692d8723a18b6c5e43356c7caac01a6">
    	<div data-embed="null" data-width="560" data-height="315">
		<img alt="thumbnail" class="thumbnail" src="assets/images/video-static.jpg">    
	</div>
    	<div class="caption">
    		<h1>example caption</h1>
    		<a class="play">Play Video</a>
    	</div>
    </div> 
```

## Banner Vimeo width Static Option HTML
Player shows a user made static image and plays a vimeo video (must have thumbnail image)
```html
    <div class="banner" data-player="vimeo-solo" data-mode="static" data-vimeo="290738166.hd.mp4?s=ee27ae407692d8723a18b6c5e43356c7caac01a6">
    	<div data-embed="null" data-width="560" data-height="315">
    		<img alt="thumbnail" class="thumbnail" src="assets/images/video-static.jpg">
    	</div>
    	<div class="caption">
    		<h1>example caption</h1>
    		<a class="play">Play Video</a>
    	</div>
    </div>
```

## Banner Youtube Player HTML
Uses a static image or generates an image from youtube api, plays a youtube video.
```html
    <div class="banner" data-player="youtube">
    	<div data-embed="yEkWVQywXIE" data-width="560" data-height="315"></div>
    	<a class="play"></a>
    </div> 
```    

## Youtube Lazyload HTML
Include a custom image thumbnail or leave the container empty to use the default high resolution image from the youtube video.
```html
	<div class="youtube" data-embed="Ivx8TAcGKP8" data-width="560" data-height="315">
		<img alt="youtube thumbnail" class="thumbnail" src="https://img.youtube.com/vi/Ivx8TAcGKP8/maxresdefault.jpg">
	</div>
```

## Links
https://codepen.io/endeart/pen/WPNBWW
