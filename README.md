# Brain-Tumor-Segmentation

About The Dataset:


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

<img width="910" alt="Screenshot 2024-06-29 at 18 17 10" src="https://github.com/Ehsan-Taheri/Brain-Tumor-Segmentation/assets/24533827/90762a28-6ffe-4a21-a29a-6e9e2600ae24">



Refrences:
https://www.sciencedirect.com/science/article/pii/S1877050920307614
https://www.nature.com/articles/s41598-021-90428-8
https://www.mdpi.com/2075-4418/13/16/2650
