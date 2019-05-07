## three-stl-net-loader

@aleeper's [THREE.STLLoader](http://threejs.org/examples/js/loaders/STLLoader.js) repackaged as a node module, with request header and credentials support

## install

`npm i --save three`

`npm i --save three-stl-net-loader`

## usage

```js

import * as THREE from 'three';
import STLLoader from 'three-stl-net-loader';

var loader = new STLLoader()

loader.setRequestHeader({ Authorization: 'Bearer token' });
loader.setWithCredentials(true);

loader.load('https://secured-api/path/to/file.stl', function (geometry) {
  var material = new THREE.MeshNormalMaterial()
  var mesh = new THREE.Mesh(geometry, material)
  scene.add(mesh)
});

```
