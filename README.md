# Welcome to the TLS Practical Repository for ARS

This is the repository for the **Advanced Remote Sensing (ARS) TLS Practical** at **UGent**.  

## What You'll Learn

In this practical, you will:  
- Gain an understanding of what **point cloud data** is and how to process it.  
- Use **the RayCloudTools library** to perform instance segmentation<sup>[1]</sup> on a plot point cloud.
- Use **CloudCompare** to manually correct instance segmentation of a tree point cloud.
- Use **the RayCloudTools library** to model tree structure from point clouds. 
- Use **the ITSMe R package** to calculate structural metrics from tree point clouds.  

---

<sup>[1] </sup>**Instance segmentation** is the process of identifying and separating individual trees or tree components within a 3D forest point cloud, assigning a unique label to each tree so that each point belongs to exactly one tree.

---

## Google colab
[Google Colab](https://colab.research.google.com/) is a free, cloud-based notebook environment developed by Google. It allows you to write and run code directly in your browser without installing anything on your own computer. We use Google Colab because everyone works in the same environment, it runs in the cloud (so it works on any laptop), files can easily be saved to Google Drive, it ensures the practical runs consistently for everyone. 

## Resources  
### Data
In the data folder (in this repository) you will find the point cloud file (.ply format) of a part of the Groenevallei park, which was scanned in the winter of 2025. This will be the basis of our practical. This point cloud was obtained after several processing step: 
1. the raw scans collected in the field were **filtered** (removing noisy points); 
2. then the scans were **aligned** into the same coordinate system so they match up spatially; 
3. then the scans were **merged** e.g. combining the point clouds of each scan into 1 point cloud;
4. the combined point cloud was **downsampled** to a resolution of 5 cm (1 point for each 5 cm cube) which reduces the size considerably (which is needed to run everything in the google colab environment).

We will automatically extract trees from this point cloud, manually correct this, model them to extract volume and extract sturctural metrics such as H, DBH and crown area. All intermediary files should be stored in this folder.

### Manuals
In the manuals folder in this repository you will find some additional files that can help you before/during/after the practical.

📌 [01_Google_Colab.md](./manuals/01_Google_Colab.md)  
This guide includes **tips and tricks** for using **Google Colab**, the environment that we're using for this practical. So if you're unfamiliar with Google Colab, feel free to explore this guide before the practical. 

📌 [02_Questions.md](./manuals/02_Questions.md)  
This file contains **all the reflection questions** from the notebooks in one place, making it easier to review and answer them during and after the practical. These questions make you reflect on what you have learned during the practical and are example questions for the exam. 

### Notebooks
In the notebooks folder in this repository you will find the notebooks that we will use during the practical to run **RCT** and **ITSMe**. 

📌 [00_ARS_TLS_practical_preparation.ipynb](./notebooks/00_ARS_TLS_practical_preparation.ipynb)  
This notebook contains all the **preparation steps** required for the practical. NOTE: This can take an hour of processing time so it needs to be completed before beginning the practical.
Instructions on opening this notebook in google colab are found below, under 'Preparation'

📌 [01_ARS_TLS_practical_RCT.ipynb](./notebooks/01_ARS_TLS_practical_RCT.ipynb)  
This notebook contains the installation of **RCT** in google colab and processing of a plot point cloud file to individual tree point clouds (and models).

📌 [02_ARS_TLS_practical_CloudCompare.md](./notebooks/01_ARS_TLS_practical_CloudCompare.md)  
This notebook contains guided steps to manipulating point clouds in **CloudCompare** for instance segmentation correction. 

📌 [03_ARS_TLS_practical_QSM.ipynb](./notebooks/02_ARS_TLS_practical_QSM.ipynb)  
This notebook contains guided steps to creating Quantitative Structure Models (QSMs) from individual tree point clouds using **RCT**.

📌 [04_ARS_TLS_practical_ITSME.ipynb](./notebooks/04_ARS_TLS_practical_ITME.ipynb)  
This notebook contains the installation of **ITSMe** in google colab and extraction of structural metrics from single tree point cloud files.

---

## Preparation

All the steps to prepare for the practical are found in the [00_ARS_TLS_practical_preparation.ipynb](./notebooks/00_ARS_TLS_practical_preparation.ipynb) notebook 

To open this first notebook, there are 2 ways:
1. navigate to the notebook in GitHub and change the github.com part of the url to githubtocolab.com OR

2. navigate to [Google Colab](https://colab.research.google.com/), click on the GitHub tab in the welcome window, and search for this repository by entering the following url:
https://github.com/qforestlab/ARS_TLS_course/tree/main 

After completing this preparation notebook, the rest of the notebooks will be cloned to your google drive and can be accessed there. Keep in mind that the setup takes about an hour and involves data download/upload, as well as R package installation.

## The practical

During the practical, you will work through notebooks 01 to 04 independently. We will be available in the room to answer any questions. At the end, please save and upload your notebooks to Ufora; detailed instructions will be provided during the session.

Each notebook contains reflection questions—these are examples of the types of questions that could appear on the exam. You are not required to answer them, but you may do so in the notebook if you wish.

---

Good luck! 🍀  

