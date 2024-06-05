# Brain-Tumor-Classification

About The Dataset
The Multimodal Brain Tumor Image Segmentation Benchmark (BRATS) is a challenge focused on brain tumor segmentation and occurs on an yearly basis on MICCAI. This dataset, from the 2015 challenge, contains data and expert annotations on four types of MRI images:

T1
T1c
T2
FLAIR
We are provided with four types of MRI for each patient.

In training dataset we are provided with two types of brain gilomas and each patient consists of 4 MRI and segmented tumor image.

In test dataset we are provided with four MRI images our task is to find the segmented image of Tumor and on the basis of this segmented tumor predict the HGG LGG gilomas

APPORACH USED FOR PROBLEM
First we preprocessed the dataset.
In preprocessing steps we use the windows tecniques(which used by the doctors to analyze the MRI)
Then adjust the pixel array according to colorspace.
Then use the masking techniques to highlight only the required part.
Then normalize and crop the images.
Then use the U-Net segmentation architecture for learining the segmentation on Brain MRI images.
We then pass the result of segmentation model to a classifier to classify in HGG and LGG.
Image Preprocessing

For reading the .mha extension file SimpleITK library is used
For visulization of the image the image is converted into 2D slices.
