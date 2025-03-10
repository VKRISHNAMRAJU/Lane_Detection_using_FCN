
# **LANE DETECTION USING FCN**
Lane detection is a crucial computer vision task that involves identifying the boundaries of driving lanes in an image or video of a road scene. It plays a vital role in various applications, particularly in the realm of autonomous vehicles and advanced driver-assistance systems (ADAS).  Convolutional neural networks (CNNs) are now the dominant approach for lane detection. Trained on large datasets of road images, these models can achieve high accuracy even in challenging situations.  In this we implemented FCN architecture which is a deep learning algorithm widely used for image segmentation.
## FCN(Fully Convolutional Networks)
Fully Convolutional Networks, or FCNs, are an architecture used mainly for semantic segmentation. They employ solely locally connected layers, such as convolution, pooling and up sampling. Avoiding the use of dense layers means less parameters (making the networks faster to train). It also means an FCN can work for variable image sizes given all connections are local. The network consists of a down sampling path, used to extract and interpret the context, and an up-sampling path, which allows for localization. 
FCNs represent a paradigm shift in computer vision by enabling pixel-wise predictions through end-to-end convolutional processing. Unlike traditional Convolutional Neural Networks (CNNs) that produce a single classification for the entire image, FCNs classify each pixel, allowing for fine-grained segmentation. 


## TuSimple Dataset
The TuSimple dataset is a large-scale dataset for autonomous driving research, focusing on lane detection and perception tasks. It's widely used in computer vision and autonomous driving communities for benchmarking and developing algorithms.

The TuSimple dataset consists of 6,408 road images on US highways. The resolution of image is 1280×720. The dataset is composed of 3,626 for training, 358 for validation, and 2,782 for testing called the TuSimple test set of which the images are under different weather conditions.



## FCN Architecuture 

![fcn_1](https://github.com/maheshmm7/Lane_Detection_using_FCN/assets/121345928/70d927ab-ee99-4ed8-a5a7-b0bba70400c4)


![fcn](https://github.com/maheshmm7/Lane_Detection_using_FCN/assets/121345928/b607da64-773c-44c4-b9aa-82412af2659a)

## Downloads :    
Download the Full Dataset Here: [TuSimple](https://www.kaggle.com/datasets/manideep1108/tusimple)

Download the PreProcessed Dataset Here: [TuSimple_Preprocessed](https://www.kaggle.com/datasets/rangalamahesh/preprocessed-1/data)

Checkout the Kaggle Link for this project : [Kaggle](https://www.kaggle.com/code/rangalamahesh/lane-detection-using-fcn)
## Getting Started 

To run this project you can download the FCN.ipynb file provided in the repository and the dataset from the download section and can implement the whole process by following the instructions in the [Kaggle Link](https://www.kaggle.com/code/rangalamahesh/lane-detection-using-fcn).  Below are the basic Requirements to run the code 

```bash
  - Tensorflow version > 2.0.0
  - Keras
  - GPU
  - CUDA
```

I choose Kaggle to implement this because it provides inbuilt GPU accelerator which accelerate the training process, I used GPU T4 x2 to implement this.  You can also choose google colab to run this, google colab also provides inbuilt GPU accelerator which fast up the training process much faster that using CPU.
## Training the Model

To train this model I used GPU T4 x2 accelerator which accelerated my trained process much more faster than using CPU.  In my model training process the training Epochs are 32, batch size is 8 and the process went well with higher accuracy and low loss. 

I used the [TuSimple_Preprocessed](https://www.kaggle.com/datasets/rangalamahesh/preprocessed-1/data) dataset to run the process.  You can prepare you own preprocessed dataset by follwing this [Link](https://www.kaggle.com/code/rangalamahesh/preprocessed).
You have to download or upload the [TuSimple](https://www.kaggle.com/datasets/manideep1108/tusimple) to prepare your own dataset.



### Test 

You can download the weights file FCN.h5 file and directly test it for predictions.  

Also find the inference_fcn.ipynb file which contained the testing or inference code.

To test the code
```bash
  Download the inference_fcn.ipynb file and load the model weights
  FCN.h5 path  and provide the testing image path in the inference code. 
  By running the inference_fcn.ipynb file you can visualize the plot of the predictions.
```

## METRICS VISUALIZATION

![FCN](https://github.com/maheshmm7/Lane_Detection_using_FCN/assets/121345928/f1d0a00d-bd26-4c74-9e3f-1e2c5548c589)


The Above graph visualize the metrics during the training process, it shows the graph showing Training & Validation Loss and Training & Validation Accuracy with the staring value and ending value.  The graphs shows the gradual decrease in the loss function and gradual increase accuracy as shown in the visualization.

You can also check the TensorBoard logs to visualize the metrics and the layers in the Architecture.

To run the TensorBoard logs follow the command in your Terminal:
```bash
tensorboard --logdir=path/to/your/logs/directory
```
After running the command, open your web browser and go to http://localhost:6006 to access the TensorBoard interface. You'll be able to navigate through the different tabs to explore the data recorded in the tensorboard v2 file.
## Predictions 
![output](https://github.com/VKRISHNAMRAJU)/Lane_Detection_using_FCN/assets/121345928/41c61a5c-f89b-4839-90ff-ba4622954efa)

![output_2](https://github.com/VKRISHNAMRAJU/Lane_Detection_using_FCN/assets/121345928/08c3ec1b-6d34-407f-a3eb-473b9dc7afdb)


I tested the Predictions on the inference code by loading the saved .h5 weights file and testing it on the new images.  The model predictions came out to be good as shown in the figures.

## 🔗 Connect with me
[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/VKRISHNAMRAJU)

