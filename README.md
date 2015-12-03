# vr-scene

The `vr-scene` element create a canvas with BABYLON JS library and give you 3 basic elements to create 3D scenes.
```
    <vr-scene>
      <vr-object name="object1" object="sphere" ></vr-object>
      <vr-light  name="light"></vr-light>
    </vr-scene>
```
    the tag vr-scene is the main element, it define by default the scene, camera and background color.
    you have aditional parameters such us animationLength (animation loop for animation time) and followme (object name that the camera follow)
```
    <vr-scene camera = "oculus" bgcolor = '{ r:0, g:0, b:1 }'>
      <vr-object name="object1" object="sphere" position='{x: 0, y: 0, z:0}' ></vr-object>
      <vr-object name="object2" object="box"  px="-5" py="5"></vr-object>
      <vr-light  name="light" intensity="0.1" ></vr-light>
    </vr-scene>
```

# vr-object
    the vr-object has the next parameters:
```
      name      : 'object name in the scene',
      object    : 'object type':

                        'sphere'  : segments, size
                        'plane'   : size
                        'cube'    : size
                        'cylinder': { height, diamTop, diamBottom, tessellation
                        'torus'   : size, thickness , tessellation
                        'import'  : "you need to set the url parameter"

      url       : 'url to import babylon objects'
      position  : {x: 0, y: 0, z:0}
                  or set individual parameters.
                  px,
                  py,
                  pz,
      rotation  : {x: 0, y: 0, z:0}
                  or set individual parameters.
                  rx,
                  ry,
                  rz,
      scale     : {x: 0, y: 0, z:0}
                  or set individual parameters.
                  sx,
                  sy,
                  sz }
```
# vr-light
    the vr-light has the next parameters:
```
      name      : 'object name in the scene',
      position  : {x: 0, y: 0, z:0}
                  or set individual parameters.
                  px,
                  py,
                  pz,
      color: {r: 0, g: 0, b:1} // all between 0..1
                  or set individual parameters.
                  cr,
                  cg,
                  cb,
      specular: {r:0.1, g:0.1, b:0.1},
      intensity: between 0..1
```
