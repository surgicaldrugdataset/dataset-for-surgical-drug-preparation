# dataset-for-surgical-drug-preparation
[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]
This repo accompanies the research paper, Point-of-view Image Dataset for Surgical Drug Preparation and contains a link to the data, scripts to visualize and process assets, and the training code described in our paper.

## Introduction
Drug-related errors are a leading cause of preventable patient harm in the clinical setting. Anesthesiologists are responsible for delivering medications during surgery, yet currently, there are no publicly available datasets that demonstrate their workflow in the operating room (OR). Our dataset consists of 395,782 images, taken from head mounted cameras affixed to anesthesia care team members during preparation for surgery. This generalizable dataset includes high quality 4K images of different anesthesia providers, operating rooms, preparation for different types of surgeries, lighting conditions, medication vials and syringes. Additionally, this study explores four baseline algorithms for two research tasks: 

1) a fast-acting neural network to identify syringes in the hand of the Anesthesia provider as well as the drug label on the syringes.
2) a classifier for drug names on the drug labels. 
3) a fast-acting neural network to identify vials in the hand of the Anesthesia provider as well as the vial label on the vials.
4)a classifier for drug names on the vial labels.

For these tasks we demonstrate performance with accuracies of over 0.9. This confirms the promise of machine learning approaches based on these types of datasets while leaving ample room for improvement to our dataset and baseline models.

## Dataset
To achieve our aims, we recorded fifty-two hours of video footage via a head-mounted camera. Most footage was captured by a trained anesthesia provider during pre-operation drug prepartion in the OR. Additional controlled environment footage was recorded by a researcher in an unoccupied OR. All footage has been de-identified of names and provider information; however, we ask that any user agree to our Terms and Conditions before downloading this dataset. Please find our data at (https://figshare.com/s/09bca8746cd868f6759c)


## Code
Our models use Python 3 to convert video footage, taken at 60 frames/second, to individual frames. Frames can be utilized to run the aforementioned four benchmarking tasks. 
Before running this model, please request our data from the above link. The data is not included in this Github repository. 

1) To enhance the model’s generalization ability, we adopt the transfer Learning method and use pre-trained Weights provided By Yolov5 and Detectron2. 
2) This task aims to train a classifier that can distinguish between the different drug labels. A total of 20 common drugs that are part of the dataset were used for this task (drug label classification).
3) To enhance the model’s generalization ability, we adopt the transfer Learning method and use pre-trained Weights provided By Yolov5 and Detectron2.
4) This task aims to train a classifier that can distinguish between the different drug labels. A total of 20 common drugs that are part of the dataset were used for this task (vial label classification).

## Contact

This code was orginally created by Solomon Nsumba. Please reach out with any questions or issues at (snsumba@gmail.com).


This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
