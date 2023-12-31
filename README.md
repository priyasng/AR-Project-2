﻿# AR-Project-2
 
## AR Alphabet Basic Project

This is a basic Augmented Reality (AR) project that showcases the alphabet letters with associated 3D models. The project uses the A-Frame framework along with AR.js to create an interactive AR experience. When using this project, you'll be able to view 3D models of different objects associated with each alphabet letter through your device's camera.

## Getting Started
To run this project on your local machine, follow the steps below:

## Prerequisites
A device with a camera (e.g., smartphone, tablet, or laptop with a webcam).
A compatible browser that supports WebXR and AR (such as the latest versions of Google Chrome or Mozilla Firefox).

## Running the Project

Clone the repository to your local machine:

git clone <repository-url>

Open the index.html file in your preferred compatible browser.

Allow the browser to access your device's camera when prompted.

Point the camera at a barcode or QR code (0, 1, 2, or 3) to trigger the corresponding alphabet letter with its 3D model.

## Supported Alphabet Letters

The project currently supports the following alphabet letters along with their associated 3D models:

A - Apple
B - Ball
C - Cat
D - Dog
E, F, G, and so on...

## Customizing and Adding More Models

You can customize this project to add more alphabet letters or replace existing 3D models. 

## Here's how you can do it:

Prepare your 3D model in the GLTF format and place it in the alphabet/<letter> directory.

Update the index.html file to add a new marker for the alphabet letter. You can copy the existing <a-marker> elements and modify them with the new type and value attributes:

html code

<a-marker type="barcode" value="<new-value>">
  <!-- Alphabet <Letter> - <Model Name> -->
  <a-entity
    position="<x> <y> <z>"
    rotation="<x> <y> <z>"
    scale="<scale> <scale> <scale>"
    gltf-model="#<model-id>"
  ></a-entity>
</a-marker>

Replace <new-value> with a unique number to identify the new letter. Modify the <Letter> and <Model Name> with the corresponding letter and the name of the 3D model. Adjust the <x> <y> <z> positions, <x> <y> <z> rotations, and <scale> values to position and scale the model properly.

Update the <a-assets> section to include the new 3D model:

html code
<a-assets>
  <!-- Existing Models -->
  <a-asset-item id="apple" src="./alphabet/apple/scene.gltf"></a-asset-item>
  <a-asset-item id="ball" src="./alphabet/ball/scene.gltf"></a-asset-item>
  <a-asset-item id="cat" src="./alphabet/cat/scene.gltf"></a-asset-item>
  <a-asset-item id="dog" src="./alphabet/dog/scene.gltf"></a-asset-item>

  <!-- New Model -->
  <a-asset-item id="<model-id>" src="./alphabet/<letter>/scene.gltf"></a-asset-item>
</a-assets>
Replace <model-id> with a unique ID for the new model and <letter> with the corresponding letter.

Save your changes and reload the index.html file in the browser to see the new alphabet letter with the 3D model.

## Acknowledgments
A-Frame: https://aframe.io/
AR.js: https://github.com/jeromeetienne/AR.js/

## Feel free to improve, modify, and use this project. Happy coding! 😊
