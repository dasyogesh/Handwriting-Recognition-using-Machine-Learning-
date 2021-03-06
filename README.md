# handwriting-recognition
Implementation of handwriting recognition using machine learning.

ABSTRACT:
Handwriting recognition is a process of transforming handwritten text into machine understandable and executable format. The objective of handwritten character recognition system is to implement user friendly computer assisted character representation that will allow successful extraction of characters from handwritten documents and to digitalize and translate the handwritten text into machine readable text. Handwriting recognition like other intelligent systems provides some application in hand phones, robots and other devices for identification and verification purposes. Active area research in handwriting includes online recognition, offline recognition, signature verification, postal- active interpretation and bank-check processing. Challenging problems in online hand writing recognition are different character sizes, different writing styles and duplicate pixels produced by hesitation in writing or interpolated non-adjacent pixels caused by fast writing. Challenging problems in online hand writing recognition are different character sizes, different writing styles and duplicate pixels produced by hesitation in writing or interpolated non-adjacent pixels caused by fast writing.


## Requirements
- [Python 3.6](https://www.python.org/downloads/)
- [TensorFlow 1.6](https://www.tensorflow.org/install/)
- [SciPy 1.0](https://scipy.org/install.html)
- [Keras 2.1](https://keras.io/#installation)
- [EMNIST dataset](https://www.nist.gov/itl/iad/image-group/emnist-dataset)

## Instructions
### Training
Before training, ensure that `emnist-byclass.mat` from the [EMNIST dataset](https://cloudstor.aarnet.edu.au/plus/index.php/s/7YXcasTXp727EqB/download) is stored within the `data/` directory.

Run the training script using:

``` bash
python3 train.py
```

A model h5, YAML, and Pickle file will be generated within the `model/` directory.

### Prediction
Once the model has been created, a handwritten character images can be predicted by running:

``` bash
python3 predict.py [file1] ...
```

Note: multiple files can be predicted in one instance and a wildcard `*` can be used to process all files within a directory.

### Drawing Prediction GUI
A Tkinter GUI with a drawing canvas has been created to test the model implementation more easily. This can be started with the command:

``` bash
python3 draw_gui.py
```

### To-do
- ~~GUI testing environment for live demo~~
- ~~Train on byclass dataset~~
- ~~Improve prediction accuracy (should improve after switching to byclass)~~
- ~~Compare byclass with other EMNIST datasets~~
- ~~Improve image preprocessing~~
- ~~Image process strings of letters~~
- Train using other learning algorithms (if time permits)
    - SVM
    - Random forest

