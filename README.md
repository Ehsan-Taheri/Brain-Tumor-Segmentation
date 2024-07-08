# Brain-Tumor-Segmentation

Data Loading and Preprocessing:

The code starts by setting a limit on the number of images to process and initializing empty lists for images and masks.
It defines functions to load NIfTI files and to get images and masks for both high-grade gliomas (HGG) and low-grade gliomas (LGG).
The get_images_and_masks function randomly samples image files, loads different modalities (FLAIR, T1, T1ce, T2), and their corresponding masks.


## Image Processing:

Functions are defined to normalize images, binarize them based on thresholds, and preprocess the images by combining binary versions of FLAIR and T2 modalities.
The select_best_slice function chooses the slice with the most information from each 3D image.


## Data Preparation:

The code processes the loaded images and masks, normalizes the images, and binarizes the masks.
It then visualizes some examples to ensure data correctness.


## U-Net Model Definition:

A U-Net architecture is defined for image segmentation. This includes an encoder path (downsampling), a bottleneck, and a decoder path (upsampling).
The model uses convolutional layers, max pooling, and upsampling operations.
It's compiled with Adam optimizer and binary cross-entropy loss.


## Model Training:

The data is split into training and validation sets.
Callbacks for model checkpointing and early stopping are defined.
The model is trained on the data, with the best model being saved.


## Model Evaluation and Visualization:

The trained model is evaluated on the validation set.
Predictions are made on the validation set and visualized alongside the original images and true masks.


## Data Augmentation:

An image data generator is created to perform data augmentation, including rotations, shifts, zooms, and flips.
Augmented images and masks are generated and visualized.


## Enhanced U-Net Model:

An improved U-Net model is defined, incorporating batch normalization layers for better training stability.


## Final Training and Evaluation:

The enhanced model is trained on the augmented dataset.
Final predictions are made and visualized.


## Performance Metrics:

Various metrics including Dice coefficient, precision, recall, and F1 score are calculated to evaluate the model's performance.
These metrics are then visualized in a bar plot.



This code represents a complete pipeline for brain tumor segmentation using MRI images, from data loading and preprocessing to model training, evaluation, and performance visualization.


<img width="910" alt="Screenshot 2024-06-29 at 18 17 10" src="https://github.com/Ehsan-Taheri/Brain-Tumor-Segmentation/assets/24533827/90762a28-6ffe-4a21-a29a-6e9e2600ae24">

![output](https://github.com/Ehsan-Taheri/Brain-Tumor-Segmentation/assets/24533827/ca65c813-d7f9-4edd-8406-2d56b7db74ba)


Refrences:
https://www.sciencedirect.com/science/article/pii/S1877050920307614
https://www.nature.com/articles/s41598-021-90428-8
https://www.mdpi.com/2075-4418/13/16/2650
