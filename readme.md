# node-cub-webshot

A modiefied Version of Kokoszka's and Whittemore's [node-webshot](https://github.com/sindresorhus/grunt-svgmin#available-optionsplugins).

## Multiple screenshots
With onCallBack-function you can create multiple screenshots in one session.

Use the callBack function on client-side to trigger a screenshot:

```javascript
if (typeof(window.callPhantom) === 'function') {
	window.callPhantom('takeShot');
}
```

And close the session with:

```javascript
if (typeof(window.callPhantom) === 'function') {
	window.callPhantom('lastShot');
}
```


Create a gulp-task like this:

```javascript
gulp.task('webshot', function() {
	return gulp.src('dist/*.html')
		.pipe($.cubWebshot({
			dest:'.tmp/screenshot/',
			root:'dist',
			takeShotOnCallback: true,
			onCallback: function(){},
		}
	));
})
```

This task loops all html-files in the folder dist and creates a screenshot if there is a callBack function in the html-file.

## License

MIT ©