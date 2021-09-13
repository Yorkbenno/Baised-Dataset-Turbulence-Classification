# 2020-Fall HKUST COMP4211-Project [Baised-Dataset-Turbulence-Classification](https://github.com/Yorkbenno/Baised-Dataset-Turbulence-Classification) 

### This is the code for the Group Project of course **Machine Learning (COMP4211) Fall-2020, HKUST**

> Since the Datasets we used are quiet large, they are provided in [this google drive link](https://drive.google.com/file/d/1IsHlusloZ0dqyS1RBsatCWf-FFSIyE5T/view?usp=sharing) for reproduction

## 1. Project description

In fluid dynamics, **turbulence** or **turbulent flow** is fluid motion characterized by chaotic changes in pressure and flow velocity. Turbulence is commonly observed in everyday phenomena such as surf, fast flowing rivers, billowing storm clouds, or smoke from a chimney, and most fluid flows occurring in nature or created in engineering applications are turbulent. 

We categorize the turbulence according to its intensity as “moderate” (MOD) or “severe” (SEV). For each reported turbulence occurrence, we are given the corresponding multispectral images (of size 224 × 224 pickle files) with the following 4 bands (or channels): (i) band 8: which detects water vapor; (ii) band 12: ozone; (iii) bands 13: infrared; and (iv) band 14: another wavelength in the infrared spectrum. we are also given some multispectral images that do not contain turbulence (class NIL)

## 2. Objectives

We need to construct our own classification network to classify those images into the aforementioned three classes. By the way, the given dataset is not balanced with the ratio of training images for three classes around 6 (SEV) : 8(MOD) : 3(NIL). The specific data count could be find in our given `ipynb` files in `model` folder. 

So proper manipulations need to be carried out to deal with this unbalanced issue.

## 3. Results

The final validation accuracy for our model is **83%** with Precision, Recall, F1 score for three classes listed below for reference:

Class NIL: 94% 85% 89%

Class MOD: 68% 85% 75%

Class SEV: 66% 64% 65%

## 4. File descriptions

The files in this repository are:

`./MyDataset.py:` The dataset python file, this part of code is incorporated into the `ipynb` files.

`./Group18-pre3.pptx:` This is our final presentation PPT which contains lucid laymen description of our model.

`./project_description.pdf:` This contains the description and instruction of our project.

`./pictures/:` Contains some relevant pictures to our presentation.

`./model/Baseline1_final.ipynb:` Our baseline 1 model.

`./model/Baseline2_final.ipynb:` Our baseline 2 model.

`./model/Final-model.ipynb:` Our baseline 3 model, also the finally utilized model.

`./model/resnet.ipynb:` Test the Resnet18 network.

`./model/resnet_normalization.ipynb:` Resnet18 with normalization.