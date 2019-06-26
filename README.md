# tensorflowJS-express-mnist
An example project for using tensorflowJS with a express web server.

![Screnshot](screenshot.png?raw=true)

# getting started
- install nodeJS and npm from official website https://nodejs.org/en/download/
- clone project
- open terminal and cd in project root folder
- execute:
    - npm i
    - node server.js
- with your browser navigate to localhost:3000

# project description
Except from the nodeJS standard files and directories this project contains:
- A MNIST-folder that contains the MNIST-data binaries. For reference: http://yann.lecun.com/exdb/mnist/
- A saved-folder that contains the saved, pretrained models. Note: If you retrain a model, the existing file will be overwritten
- server.js - this file contains the server logic. It starts a webserver, that serves a static HTML frontend, loads a pretrained model and listens for requests to predict, that contain a 28x28 number array, representing an image.
- mnist.js - this file trains a feedworward neural network to recognize handwritten digits, with the MNIST data.
- convolutional-mnist.js - this file trains a convolutional neural network to recognize handwritten digits, with the MNIST data.
- maximum.js - this file trains a feedworward neural network to recognize the index of the maximum value of an array. The training data is generated automatically.
- canvas.html - this file is the frontend, that the server serves. It contains a drawable canvas and javascript functions, that translate the canvas-bitmap to an appropriate array and reshape it (centering of the image regarding it's center of mass). A function that sends this data within a http-request to localhost:3000/api/predict is called every 5 seconds.

