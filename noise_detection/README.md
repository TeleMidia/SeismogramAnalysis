# Seismic Noise Detector (SND)
This repository contains the source code and dataset used in the work "Seismic Shot Gather Noise Localization Using a Multi-Scale Feature-Fusion-Based Neural Network" (Under review).

## Installation

Install Python > 3.6 
  * https://www.python.org/downloads/

With pip, install the following dependencies:

    $ pip install tensorflow-gpu (>= 1.9.0)
    $ pip install numpy
    $ pip install matplotlib
    $ pip install opencv-python
    $ pip install xtarfile
    $ pip install zip-files
    $ pip install setuptools
    $ pip install collections-extended

Install the TensorFlow Object Detection API

  * https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2.md


## Dataset

Extract dataset files from  `src/dataset.rar`

Dataset Content:

  * 6500 seismograms
  * 65 VoTT annotation files (https://github.com/microsoft/VoTT)
  * train.txt, valid.txt and test.txt (seismograms of the training, validation and test set, respectivelly).
  * train.record, valid.record and test.record (sets exported to tfrecord format)
  
## Using the SND for inference
Copy the `seismic_noise_detectior.ipynb` file into the `object_detection` folder of TensorFlow Object Detection API. With Jupyter notebook, run:

    $ jupyter notebook

Next, open the `seismic_noise_detectior.ipynb` file and follow the step-by-step described in it.

## Training and Evaluation

To train and evaluate your own model, follow these [tutorial](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1.md)

You can use the models created by this work as a reference. They are in the src / models folder:

  * ssd_mobilenet_v1.config (SSD + MobileNet v1)
  * ssd_inception_v3 (SSD + Inception v3)
  * ssd_resnet_50 (SSD + Resnet-50)
  * ssd_mobilenet_v1_fpn (SSD + MobileNet v1 + FPN)
  * ssd_mobilenet_v1_focal_loss (SSD + MobileNet v1 + Focal loss)
  * ssd_mobilenet_v1_fpn_focal_loss (SSD + MobileNet v1 + FPN + Focal loss)
  


