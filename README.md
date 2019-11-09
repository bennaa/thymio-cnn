## Universita' della Svizzera Italiana - Robotics Final project
## Real robot place recognition using Convolutional Neural Network (CNN) and ROS
### Authors: [Andrea Bennati](https://github.com/bennaa) & [Alessio Della Libera](https://github.com/dellalibera)
This repository contains our final project for Robotic Course.

The goal of this project is to use the [Thymio](https://github.com/jeguzzi/mighty-thymio) robot to predict in which place it is.

Python Version: 2.7

The libray used are:
* pytorch v1.1
* openCV (cv2)
* matplotlib
* numpy
* ROS (melodic version)
* [keyboard library](https://github.com/boppreh/keyboard)

The following code has been tested only on Ubuntu 18.04.

## Control Usage
`python main.py main.py [-h] [--action {random_walking,human,stop}] --name NAME [--save_image SAVE_IMAGE] [--path_save_image PATH_SAVE_IMAGE] [--predict PREDICT] [--render RENDER] [--record RECORD] [--path_model PATH_MODEL]`

### Examples
#### Random Walking (moving and save images)
`python main.py main.py --action random_walking --name thymio23 --save_image True --path_save_image /path/to/directory`

#### Human Control (moving and predict)
`python main.py main.py --action human --name thymio23 --predict True --path_model /path/to/saved/model`

## CNN Usage
`python Thymio_cnn.py [-h] --src SRC [--path_model PATH_MODEL] [--action {train,display}]`

### Examples
#### Train the CNN
`python Thymio_cnn.py --src /path/to/images/ --action train`

#### Display Images
`python Thymio_cnn.py --path_model /path/to/saved/model`
