# Welcome to the TLS Practical Repository for ARS

This is the repository for the **Advanced Remote Sensing (ARS) TLS Practical** at **UGent**.  

## What You'll Learn  

In this practical, you will:  
- Gain an understanding of what **point cloud data** is and how to process it.  
- Use **the RayCloudTools library** to perform instance segmentation on a plot point cloud.  
- Use **CloudCompare** to manually correct instance segmentation of a tree point cloud.
- Use **the RayCloudTools library** to model tree structure from point clouds. 
- Use **the ITSMe R package** to calculate structural metrics from tree point clouds.  

This repository contains all the necessary files to **successfully complete the practical**.  

---

## Google colab
[Google Colab](https://colab.research.google.com/) is a free, cloud-based notebook environment developed by Google. It allows you to write and run code directly in your browser without installing anything on your own computer. We use Google Colab because everyone works in the same environment, it runs in the cloud (so it works on any laptop), files can easily be saved to Google Drive, it ensures the practical runs consistently for everyone. 

## Resources  
### Data
In the data folder in this repository you will find the point cloud file (.ply format) of a part of the groenevallei park, which was scanned in the winter of 2025. This will be the basis of our practical. We will extract trees from this point cloud, model them to extract volume and extract sturctural metrics such as H, DBH and crown area.

### Manuals
In the manuals folder in this repository you will find some additional files that can help you before/during/after the practical.

📌 [01_Google_Colab.md](./manuals/01_Google_Colab.md)  
This guide includes **tips and tricks** for using **Google Colab**, the environment that we're using for this practical. So if you're unfamiliar with Google Colab, feel free to explore this guide before the practical. 

📌 [02_Questions.md](./manuals/02_Questions.md)  
This file contains **all the questions** from the notebooks in one place, making it easier to review and answer them during and after the practical. These questions make you reflect on what you have learned during the practical and are example questions for the exam. 

### Notebooks
In the notebooks folder in this repository you will find the notebooks that we will use during the practical to run RCT and ITSMe. 

📌 [00_ARS_TLS_practical_preparation.ipynb](./notebooks/00_ARS_TLS_practical_preparation.ipynb)  
This notebook contains all the preparation steps required for the practical. NOTE: This can take an hour of processing time so it needs to be completed before beginning the practical.
Instructions on opening this notebook in google colab are found below, under 'How to Get Started'

📌 [01_ARS_TLS_practical_RCT.ipynb](./notebooks/01_ARS_TLS_practical_RCT.ipynb)  
This notebook contains the installation of **RCT** in google colab and processing of a plot point cloud file to individual tree point clouds and models.

📌 [02_ARS_TLS_practical_CloudCompare.ipynb](./notebooks/01_ARS_TLS_practical_CloudCompare.md)  
This notebook contains guided steps to manipulating point clouds in CloudCompare for segmentation correction. 

📌 [03_ARS_TLS_practical_QSM.ipynb](./notebooks/02_ARS_TLS_practical_QSM.ipynb)  
This notebook contains guided steps to creating Quantitative Structure Models (QSMs) from individual tree point clouds using RCT.

📌 [04_ARS_TLS_practical_ITSME.ipynb](./notebooks/04_ARS_TLS_practical_ITME.ipynb)  
This notebook contains the installation of **ITSMe** in google colab and extraction of structural metrics from single tree point cloud files.

---

## How to Get Started  

All the steps to get started are found in the 00_ARS_TLS_practical_preparation.ipynb notebook.
To open this first notebook, navigate to [Google Colab](https://colab.research.google.com/), click on the GitHub tab in the welcome window, and search for this repository by entering the following url:
https://github.com/qforestlab/ARS_TLS_course/tree/main

After completing the setup notebook, the rest of the notebooks will be cloned to your google drive and can be accessed there.
Keep in mind that the setup takes about an hour and involves data download/upload, as well as R package installation.

---

Good luck! 🍀  

