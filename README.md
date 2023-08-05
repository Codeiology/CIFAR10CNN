<p>
  <img src="https://3b1b-posts.us-east-1.linodeobjects.com//images/topics/neural-networks.jpg" alt="logo" width=500/>
</p>

# CIFAR10CNN

A user friendly Flask web interface for a Convolutional Neural Network I designed, trained off of the CIFAR 10 dataset with the help of python and 
Tensorflow.

# Setup and Quickstart guide

Note: this has only been tested on my M1 mac.

Navigate to a Terminal, (make sure it has git, python3, and pip3 installed) and enter the following commands in order:


`git clone https://github.com/Codeiology/CIFAR10CNN`

`cd CIFAR10CNN`

`pip3 install -r requirements.txt`

`python3 main.py`


It might have to load for a bit before it starts. It may show a warning, but please disregard it. In a browser, navigate to:


`http://localhost:5000/`


And the web interface will render. If you are using a different computer on the network than the machine the interface is running on:

`http://(your local ip addr):5000/`

Replace (your local ip addr) with the machine that the interface is running on's private IP address. Make sure both machines are connected to the same WiFi.

IMPORTANT: The webserver won't work unless you keep the terminal running.

# Features

CIFAR10CNN can distinguish the following things apart in a photo with 80% accuracy:

`airplane`

`car`

`bird`

`cat`

`deer`

`dog`

`frog`

`horse`

`boat`

`truck`

# What is a CNN?

A CNN, or Convolutional Neural Network, is a type of AI that is constructed with "neurons". It is different from a DNN (a Dense Neural Network) because a DNN is slightly more simple and arguably worse at it's job. A CNN has rows of neurons called layers. They all do a different job.

`input layer`:

The input layer of neurons processes the images into numbers and arrays the rest of the neural network can interpret.

`convolutional layer`:


The convolutional layer has many "filters" for the data (mostly just algorithims and number functions) with parameters that are ajusted as the neural network learns.

`pooling layer`:

The pooling layer "summarizes" the data. It compresses it significantly into a single value.

Note: There can be many convolutional layers and pooling layers. CIFAR10CNN has a convolutional layer, a pooling layer, another convolutional layer, and another pooling layer.

`dropout layer`:

The dropout layer compares the data from all the neurons in the convolutional and pooling layer, and makes the final decision, which is outputted.
The full layout of the neurons in CIFAR10CNN's brain are visualized here:

![cifar10cnn](https://github.com/Codeiology/CIFAR10CNN/assets/131825227/5201e78c-282d-443d-9300-800065bede80)

# Directory guide


`main.py`: The backend functions and initializer for the webserver.

`static/compressed/`: The compressed images being fed into the AI. (I left a sample image called compressed.jpg you can test with the network!)

`static/uploads`: The images uploaded before they are compressed. (I left a sample image called boat.png)

`models/cifar10cnn.h5`: The main CIFAR10CNN model file. (binary)

`templates/aipage.html`: The main homepage HTML file for the webserver.

`templates/ohno.html`: An error message HTML file for incase the wrong filetype is uploaded.

`templates/good.html`: The HTML code for presenting the AI's output to the user.

`requirements.txt`: The requirements file for `pip3`. You can delete it after everything runs well.


Make sure to clean the static/compressed and static/uploads folders often! There is currently no function to autoclear it.
