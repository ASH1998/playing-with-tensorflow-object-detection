# playing-with-tensorflow-object-detection
This is a play code for me to get acquainted with tensorflow object detection api


## These are some sample images trained with the api :

![image1](https://user-images.githubusercontent.com/23384411/29742711-7c7fc0d8-8aa1-11e7-9081-1a570f5112b8.png)

![image3](https://user-images.githubusercontent.com/23384411/29742730-ba778876-8aa1-11e7-9c7e-2972aa3878bc.png)


![image5](https://user-images.githubusercontent.com/23384411/29742735-cc4c1490-8aa1-11e7-9c0a-36135176ae5d.png)

# Useful links :
There are a lot of dependencies and installation procedure
check out this link :
[Models of tensorflow api](https://github.com/ASH1998/models)
clone this link and go to object_detection directory and paste the code

# Installation

## Dependencies

Tensorflow Object Detection API depends on the following libraries:

* Protobuf 2.6
* Pillow 1.0
* lxml
* tf Slim (which is included in the "tensorflow/models" checkout)
* Jupyter notebook
* Matplotlib
* Tensorflow

For detailed steps to install Tensorflow, follow the
[Tensorflow installation instructions](https://www.tensorflow.org/install/).
A typically user can install Tensorflow using one of the following commands:

``` bash
# For CPU
pip install tensorflow
# For GPU
pip install tensorflow-gpu
```

The remaining libraries can be installed on Ubuntu 16.04 using via apt-get:

``` bash
sudo apt-get install protobuf-compiler python-pil python-lxml
sudo pip install jupyter
sudo pip install matplotlib
```

Alternatively, users can install dependencies using pip:

``` bash
sudo pip install pillow
sudo pip install lxml
sudo pip install jupyter
sudo pip install matplotlib
```

## Protobuf Compilation

The Tensorflow Object Detection API uses Protobufs to configure model and
training parameters. Before the framework can be used, the Protobuf libraries
must be compiled. This should be done by running the following command from
the tensorflow/models directory:


``` bash
# From tensorflow/models/
protoc object_detection/protos/*.proto --python_out=.
```

## Add Libraries to PYTHONPATH

When running locally, the tensorflow/models/ and slim directories should be
appended to PYTHONPATH. This can be done by running the following from
tensorflow/models/:


``` bash
# From tensorflow/models/
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```

Note: This command needs to run from every new terminal you start. If you wish
to avoid running this manually, you can add it as a new line to the end of your
~/.bashrc file.

# Testing the Installation

You can test that you have correctly installed the Tensorflow Object Detection\
API by running the following command:

```bash
python object_detection/builders/model_builder_test.py
```
## Custom Images
And to make sure the test images i used or for you to use custom images 
go to object_detection directory and test_images subdirectory and rename the images and change in program at " In[8] " at TEST_IMAGE_PATHS in range according to image number

Enjoy!!

## Disclaimer 
This program is owned with tensorflow. I just created some simple images file to study more about its workflow.!!
