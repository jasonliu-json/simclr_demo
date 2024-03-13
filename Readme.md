## SimCLR Fine-tuning Demo 
In this demo, we fine-tune a SimCLR model with ResNet-18 backbone to learn differences between unlabelled images and test its accuracy on a labelled dataset. 


The Simple Framework for Contrastive Learning of Visual Representations (SimCLR) 
is a self-supervised learning framework designed to learn visual representations without labeled data by leveraging contrastive learning. It generates pairs of augmented images from the same source image, using a neural network to extract features and a contrastive loss function to bring features of similar images closer while pushing dissimilar ones apart in the feature space. This process enables the model to learn useful image representations that can be fine-tuned for various downstream tasks with minimal labeled data.


### Setup 
- GPU with CUDA support is required. 
- Originally built with python 3.9.13 and CUDA 12.4 on Windows 11 

Install the packages 
```angular2html
pip install -r requirements.txt
```
Start the Jupyter notebook 
```angular2html
jupyter notebook
```

### Dataset 
The dataset used in this demo is labelled firefighting devices. It contains 148 images each with 10-20 annotations for 42 different symbols. 
https://universe.roboflow.com/yaid-pzikt/firefighting-device-detection/dataset/6

### Notes and TODO:
This demo originally started as a coding challenge for a computer vision engineering position. 
More comprehensive hyperparameter testing, particularly the batch size and other model backbones could be explored. 

Before production ready, some more tests that should be performed include:
- Classification accuracy using other methods, such as SVM
- Transfer learning performance on new unseen symbols, or on a different dataset
- Examples under more various conditions such as lighting, angles, image resolution
