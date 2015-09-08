# node-cub-webshot

A modiefied Version of Kokoszka's and Whittemore's [node-webshot](https://github.com/sindresorhus/grunt-svgmin#available-optionsplugins).

## Multiple screenshots
With onCallBack-function you can create multiple screenshots in one session.

Use the callBack function on client-side to trigger a screenshot:

```javascript
if (typeof(window.callPhantom) === 'function') {
	window.callPhantom('takeShot');
}
});

Close the session with:

```javascript
if (typeof(window.callPhantom) === 'function') {
	window.callPhantom('lastShot');
}
});

## License

MIT ©