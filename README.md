# Master IBM Maximo Visual Inspection APIs - Create an Image Inferencer & Inspection Report in 37 minutes

**Last Updated** ⏰ 07 July 2025 <br>
**Author** 👨‍💻 <a href="https://www.linkedin.com/in/christophe-lucas-a5abab28/" target="_blank">Christophe Lucas</a> [with the help of his local <a href="https://www.linkedin.com/feed/update/urn:li:activity:7345223975897088000/" target="_blank"> Multi LLM System for 💬 Q&A + 👩‍💻 Coding + 📄 Doc Interrogation</a> machine].<br>
**Disclaimer** ⚠️ This code is delivered as-is and is NOT formal IBM product or documentation in any way.

## 🌎 Recipe Overview
**Description**: In this recipe, you will first discover the IBM Maximo Visual Inspection (MVI) REST APIs and learn how to use them locally in a Jupyter notebook. Then, you will build a tkinter user interface which will allow you to load an image, infer it using an MVI model, display it with the detected defects drawn on it, and generate an inspection report providing counts of defects found and the overall area they occupy.<br>

**IBM Product Used**: <a href="https://www.ibm.com/docs/en/masv-and-l/maximo-vi/cd" target="_blank">IBM Maximo Visual Inspection</a> (MVI) version `9.0.6`, part of the <a href="https://www.ibm.com/products/maximo" target="_blank">IBM Maximo Application Suite</a> (MAS).   

**Expected Duration**: 37 minutes the first time, 3.7 minutes the second , 37 seconds after.<br>

**Prerequisites**: In order to run this recipe, all you need is
(a) a MAS user ID with `Administrator` MVI-application access to an MVI instance, 
(b) a Python virtual environment within which you'll install Jupyter Lab  to run the Notebook.
This recipe was executed with Python 3.12.7 on a Mac but similar steps can be executed on a PC - refer to <a href="https://docs.python.org/3/library/venv.html" target="_blank">Python virtual environment</a> and <a href="https://jupyter.org/install" target="_blank">Jupyter Lab </a> documentation for non-Mac users.

**Note**: With this notebook, you will be provided with ready-to-use MVI data sets (i.e. movies of solar panels containing `LichenGrowth` or `BirdDrop` defects) and models that were created as part of this <a href="https://github.com/IBM/mas-drone-to-fix-watsonx" target="_blank">From Drone to Fix - Solar Farm Inspection using IBM Maximo & Watsonx</a> show. Note however that if you have existting deployed models in MVI and images to test, you can use them - all the API calls herein should work with *any* MVI Object Detection or Segmentation model.

## 🏁 Get Ready
### Setup your local Jupyter Lab environment

Open your Mac `Terminal` and install and activate a Python `venv`:
1.  Run `mkdir mas-mvi-master-api` to create a `mas-mvi-master-api` folder. Run `cd mas-mvi-master-api` to move to that new folder.
2. Run `python3 -m venv venv` to create a virtual environment called `venv`. Once done, check that you have a `venv` folder under `mas-mvi-master-api` and that it contains the subfolders `bin`, `include`, `lib` and a file `pyvenv.cfg`.
3. Run `source venv/bin/activate` to activate the `venv`. Note that once this command is executed, a `(venv)` should appear on the left of your Terminal command line - meaning your venv is activated successfully.
4. Run `pip list` and note that only e.g. `pip 24.2` is returned i.e. your venv has no other python package installed yet.

Install and run `Jupyter Lab` in the `venv`:
1. Run `pip install jupyterlab` to Install Jupyter Lab.
2. Run `pip list` and notice that many packages have been installed that Jupyter Lab uses.
3. Run `jupyter lab`. This should ultimately invite you to open a `http://localhost:8888/lab` link in your browser. Open the link.

## 🚀 GO !
This recipe is all about running 1 notebook, step by step until the end.<br> 
Download the notebook here [mas-mvi-master-api.ipynb](https://github.com/IBM/mas-mvi-master-api/blob/main/notebooks/cl-mas-mvi-master-api.ipynb).<br>
Drag and drop it to the left window of your jupyter lab environment (`File Browser` view) running on `http://localhost:8888/lab`.<br>
Click on the Jupyter `Table of Contents` view (left).
Follow the notebook cells one after the other, in order ... <br>
Here an overview of what you'll achieve with it - Have fun !

![image](/files/mas-mvi-master-image001.jpg)
