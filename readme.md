# OyanaChan

**The quick & easy way to compile basic website** (js, scss, imgs, svg)


> OyanaChan is a rebuild version of [gulp-oyana](https://github.com/Oyana/oyanachan/tree/gulp-oyana).

OyanaChan is made for:
* Node > 12
* NPM > 6
* Gulp > 4

If you have to used older teck please consider used [gulp-oyana](https://github.com/Oyana/oyanachan/tree/gulp-oyana) insted.

## How to install

**If you havent gulp.**
* Unix: `sudo npm install gulp -g`.
* Windows: `npm install gulp -g`.

**If you havent create your `package.json` yet.**
* `npm init`

**Install**
* `npm install oyanachan --save-dev`.

## How to use

In your `gulpfile.js`.
> Use only the options you **need**!

```javascript
	const oyana = require('oyanachan');

	oyana({
		'jsMinPath' : './public/js',
		'jsPath' : './resources/js',
		'jsName' : 'main.min',
		'cssPath' : './public/css',
		'scssPath' : './resources/scss',
		'outputStyle' : 'compressed',
		'imgMinPath' : './public/img',
		'imgPath' : './resources/img',
		'htmlMinPath' : './htmlMin',
		'htmlPath' : './html',
		'htmlPages' : {
			'index.html':[
				'html/head.inc.html',
				'html/header.inc.html',
				'html/home.inc.html',
				'html/footer.inc.html',
				'html/foot.inc.html'
			]
		},
		'proxyPath' : 'http://localhost'
	});
```
   If you dont need js complation remove `{jsMinPath, jsPath, jsName}`.
   If you dont need scss complation remove `{scssPath, cssPath, outputStyle}`.
   If you dont need images complation remove `{imgMinPath, imgPath}`.
   If you dont need browser sync remove `{proxyPath}`.
   If you dont need browser sync remove `{proxyPath}`.

## Command line:

| Command | Effect | Alias |
|--------|-------|-------|
| `gulp js-compile` | Compile all js from `jsPath`  to `jsMinPath`. | `gulp js`, `gulp jquery`, `gulp script`  |
| `gulp js-compile-silent` | Compile all js from `jsPath`  to `jsMinPath` without notification. |   |
| `gulp scss-compile` | Compile all scss from `scssPath`  to `cssPath` in `outputStyle`.| `gulp scss`, `gulp sass`, `gulp compass`, |
| `gulp scss-compile-silent` | Compile all scss from `scssPath`  to `cssPath` in `outputStyle` without notification. |   |
| `gulp html-compile` | Compile all html, svg, html, plain text from `htmlPath`  to `htmlMinPath` you have to customise the hiercht throuw `htmlPages`.|   |
| `gulp html-compile-silent` | Compile all html, svg, html, plain text from `htmlPath`  to `htmlMinPath` you have to customise the hiercht throuw `htmlPages` without notification. |   |
| `gulp img-minimize` | Minimize all Images from `imgPath` to `imgMinPath`. | `gulp img`, `gulp image`, `gulp images`, `gulp minimize` |
| `gulp img-minimize-silent` | Minimize all Images from `imgPath` to `imgMinPath` without notification. | |
| `gulp watch` | Watch all scss, js, img and compile on update. |   |
| `gulp watch-silent` | Watch all scss, js, img and compile on update without notification. |   |
| `gulp oyana` | Compile all files then watch it. | `gulp` `gulp oyanachan` |
| `gulp oyana-silent` | Compile all files then watch it without notification. | `gulp *` |

## Any issue with SCSS compilation?

[Gulp SASS common issues-and their fixes](https://github.com/dlmanning/gulp-sass/wiki/Common-Issues-and-Their-Fixes#partials-sporadically-not-found)
