# Malaria Cell Segmentation Using Machine-Learning & Deep-Learning

# Data
Data came from three different labs’ ex vivo samples of P. vivax infected patients in Manaus, Brazil, and Thailand. The Manaus and Thailand data were used for training and validation while the Brazil data were left out as our test set. Blood smears were stained with Giemsa reagent, which attaches to DNA and allow experts to inspect infected cells and determine their stage.

It can be downloaded from [Kaggle](https://www.kaggle.com/kmader/malaria-bounding-boxes)


# Usage
Clone the repository and run the following commands from the terminal.

Then download the dataset from given link and copy and paste the data into input folder. All the images from dataset should be put into "input/training_images" folder.

#### Setup Tensorflow Object Detection API
Go through this [blog](https://medium.com/@marklabinski/installing-tensorflow-object-detection-api-on-windows-10-7a4eb83e1e7b) to setup TFOD on your system.

#### Install project dependencies from requirements.txt
```
 pip install -r requirements.txt
```
#  Files
<b>[preprocessing.py](https://github.com/Anaskaysar/Malaria-Cell-Segmentation-Using-Machine-Learning-and-Deep-Learning/blob/main/preprocessing.py)</b><br>
As data is present in json file this file creates annotated csv files which will be required by our Tensorflow Object Detection API.

<b>[plotting.py](https://github.com/Anaskaysar/Malaria-Cell-Segmentation-Using-Machine-Learning-and-Deep-Learning/blob/main/plotting.py)</b><br>
Script for plotting of bouding boxes of RBC, NON RBC on images.

<b>[CellExtractor.py](https://github.com/Anaskaysar/Malaria-Cell-Segmentation-Using-Machine-Learning-and-Deep-Learning/blob/main/CellExtractor.py)</b><br>
Script for cropping and extracting NON-RBC images using bounding boxes from main image for the training of VGG-16 model.
