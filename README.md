[![view on npm](http://img.shields.io/npm/v/jscad-raspberrypi.svg)](https://www.npmjs.org/package/jscad-raspberrypi) [![npm module downloads](http://img.shields.io/npm/dt/jscad-raspberrypi.svg)](https://www.npmjs.org/package/jscad-raspberrypi)

# jscad-raspberrypi

![bplus example](jsdoc2md/bplus.png)

This is a collection of jscad parts that model a RaspberryPi BPlus and various Hats.  These models use the [jscad-utils](https://github.com/johnwebbcole/jscad-utils) library and return jscad-utils [`group` objects](https://github.com/johnwebbcole/jscad-utils#utilgroupnames-objects--object).


## Installation
Install `jscad-raspberrypi` using NPM:

```bash
npm install --save jscad-raspberrypi
```

## Basic usage
To use the utilities, you need to include the `jscad-raspberrypi.jscad` file and a copy of `lodash`.

```javascript
include('node_modules/jscad-utils/jscad-utils.jscad');
include('node_modules/jscad-raspberrypi/jscad-raspberrypi.jscad');
include('node_modules/lodash/lodash.js');

main() {
  util.init(CSG);

  var BPlus = RaspberryPi.BPlus();

  return BPlus.combine();
}
```

## Yeoman Generator
You can use the [yeoman jscad generator](https://www.npmjs.com/package/generator-jscad) which will create a project that uses this library.

Once you create your project, install `jscad-raspberrypi`, and run `gulp`.  Dragging the `dist` directory into [http://openjscad.org/](http://openjscad.org/) will include this library.

Modify your `main.jscad` file to return a RaspberryPi object.

```javascript
// include:js
// endinject
/* exported main, getParameterDefinitions */
/* globals piexample */


function main(params) {

    util.init(CSG);

    return RaspberryPi.BPlus().combine();
}
```

## Reference

### RaspberryPi

* [RaspberryPi](#module_RaspberryPi)
    * [.BPlus()](#module_RaspberryPi.BPlus)
    * [.Hat()](#module_RaspberryPi.Hat)
    * [.PiTFT24()](#module_RaspberryPi.PiTFT24)
    * [.CameraModule()](#module_RaspberryPi.CameraModule)

<a name="module_RaspberryPi.BPlus"></a>

### RaspberryPi.BPlus()
Returns a complete RaspberryPi B Plus model.
![bplus example](jsdoc2md/bplus.png)

**Kind**: static method of <code>[RaspberryPi](#module_RaspberryPi)</code>  
<a name="module_RaspberryPi.Hat"></a>

### RaspberryPi.Hat()
Returns an empty Pi Hat.
![hat example](jsdoc2md/hat.gif)

**Kind**: static method of <code>[RaspberryPi](#module_RaspberryPi)</code>  
<a name="module_RaspberryPi.PiTFT24"></a>

### RaspberryPi.PiTFT24()
Returns an Adafruit PiTFT 2.4 Hat with buttons.
![PiTFT 2.4 example](jsdoc2md/pitft24.png)

**Kind**: static method of <code>[RaspberryPi](#module_RaspberryPi)</code>  
<a name="module_RaspberryPi.CameraModule"></a>

### RaspberryPi.CameraModule()
Returns an Pi camera module.
![camera example](jsdoc2md/camera.png)

**Kind**: static method of <code>[RaspberryPi](#module_RaspberryPi)</code>  

&copy; 2016 John Cole <johnwebbcole@gmail.com>. Documented by [jsdoc-to-markdown](https://github.com/75lb/jsdoc-to-markdown).
