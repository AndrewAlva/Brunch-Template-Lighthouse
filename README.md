# Frontend boilerplate (Lighthouse optimized)
This is a quickstart for small frontend projects aiming to be shipped fast but still following best practices for performance and cool experiences which includes animation and experimental interactions.

Currently more focused on single pages, but still useful for multiple pages websites.

## Google Lighthouse optimizations included
### Defer scripts
* Inline "critical" CSS & JS to avoid render blocking
* Defers load of other assets and scripts


### Lazy load images ([lazysizes.js by Alexander Farkas](https://github.com/aFarkas/lazysizes))
* Includes standard responsive image support (picture and srcset)
* Responsive image support
* SEO improved: lazysizes does not hide images/assets from Google.
* For more info about this library, check the GitHub repo mentioned above


### PWA setup files and assets
* Service Worker
* Manifest
* Icons examples


## Frontend tools and features
### Single production minified CSS and JS files.


### Modular approach
* Using jade preprocessor for HTML and
* SCSS for CSS files
* Brunch will take care of compile all js files placed in `js` folder into a single file and uglify it.


### 2 Grid systems based on SCSS vars and formulas/functions to set and calculate:
* Flexible features:
	* Columns (as many as you want)
	* Gutters
	* Left/right margin of the whole grid

* a) Media queries oriented (grid-media-queries.scss)
	* Define multiple tresholds based on 6 prestablished media queries:
		* xs => 	$mobile-large-min-width: 	576px; 		
		* sm => 	$tablet-min-width: 			768px; 			
		* md => 	$small-laptop-min-width: 	1025px; 		
		* lg => 	$laptop-min-width: 			1200px; 			
		* xl => 	$small-desktop-min-width: 	1441px;		
		* xxl => 	$desktop-min-width: 		1650px; 			

* b) 2 different versions: Mobile (Touch devices) & Desktop (Non-touch devices) (grid-2-versions.scss)* [Coming Soon]
	* Important: still in progress.
	* Oriented for viewport proportion designs (`vw` and `vh` units)
	* Also useful to create 2 different styles based on how will user interact (touch or with a pointer device like a mouse, trackpad or pen, etc.)
	* This interaction requires a mobile detection library like [Mobile-Detect by Şerban Ghiţă](https://github.com/serbanghita/Mobile-Detect) or [mobile-detect.js by Heinrich Goebl](https://github.com/hgoebl/mobile-detect.js)


### Cascade animations SCSS system (`cascade-animations.scss`)
* Delay system based on CSS attributes
* Separated on 2 possible scenarios: Mobile and Desktop
* Media query breakpoint is variable for you to decide when delays should change


### JS listener for elements inside viewport (`inview.js`)


### Complete list of metatags for sharing crawlers
* Open graph tags (og:--)
* Twitter tags
* Favicon tags
* Google Structured Data Tags


### Favicon examples
* Full list of favicon sizes
* sitemanifest setup file


### Typefaces hierarchy (`typefaces.scss`)
Global hierarchy to facilitate texts styling and follow DRY principle.


### SCSS mixins
* -webkit- prefixes included in most common properties to expand coverage.
* Short writing for:
	* Flexbox
	* Keyframe animations
	* Transforms
	* Transitions and Delays


### Throttle & Debounce JS optimizers from [Lodash](https://lodash.com/)


## Basic server configuration (only for Apache servers)
### .htaccess example
* HTTPS redirection
* .html suffix removal



## Upcoming updates
* Optional frontend features* [Coming Soon]
	* Smooth vertical scroll (full page)
	* Smooth vertical scroll (per section)
	* HTML 5 Canvas 2D
	* WebGL Basic Utilities
	* Horizontal scroll (on desktop devices)



* Compatible libraries already tested* [Coming Soon]
These libraries have been used in combination with this boilerplate, but they are not included in the core, you must integrate them by yourself downloading the files into your repo or using a CDN, as you prefer.

	* [locomotive-scroll by Locomotive](https://locomotivemtl.github.io/locomotive-scroll/)
	* [three.js by Ricardo Cabello (aka Mr.doob)](https://threejs.org/)
	* [blotter.js by Bradley Griffith](https://blotter.js.org/)
	* [p5.js started by Lauren McCarthy](https://p5js.org/)


* Overall optimization with [Juan Fuentes](https://codepen.io/JuanFuentes/).





# Built on npm and Brunch

## Development Environment
Hi there, this project is built by npm and brunch. It's coded oriented to use "modules" and "objects" of HTML and CSS with Jade and SCSS.

### Getting to know Brunch

* Install (if you don't have them):
    * [Node.js](http://nodejs.org): `brew install node` on OS X (and if you have Homebrew, if you don't go or work over Windows or Linux go check directly the documentation at Node)
    * [Brunch](http://brunch.io): `npm install -g brunch`
    * Brunch plugins and app dependencies: `npm install`
* Learn:
    * `public/` dir is fully auto-generated and served by HTTP server.  Write your code in `app/` dir.
    * Place static files you want to be copied from `app/assets/` to `public/`.
    * [Brunch site](http://brunch.io), [Getting started guide](https://github.com/brunch/brunch-guide#readme)


### Installation of this repo

1. Clone this repo in your dev environment, you can simply run:
```console
foo@bar:~$ git clone https://github.com/AndrewAlva/Brunch_Sass_Jade_Boilerplate.git
```

2. Then install node modules through npm:
```console
foo@bar:~$ npm install
```

And that's it; now you are able to work on this repo.

Also, you can watch files and compile them live while you're working with this command:
```console
foo@bar:~$ brunch w -s --port 3000
```
The last number is the port where you'd like to view the page, you can use whatever you want: 8000, 1111, etc. For mor commands visit [Brunch documentation.](http://brunch.io/docs/commands)


### Get final files for production

When you finish editing the project, you can run this code to get the final assets for production:
```console
foo@bar:~$ brunch build --production
```

This builds minified files ready to upload to server.


