# Data Science Challenge NetworkAndesAI

Welcome to the data science challenge, your goal is to create a machine learning model able to identify traffic signals from images. 

The challenge contains a directory called **traffic_Data** which includes training and testing data:
- The training data is contained into the **DATA** folder, this folder contains a folder with images for each class.
- The testing data can be found into the **TEST** folder, this folder contains several images named after it class. The class of each image will be the first three characters of the file name. 
- Finally there is a file called **labels.csv** which contains the name of the signal for each class, this will be the labels humans use to identify these signals. 

<p align="center">
  <img src="./traffic_Data/TEST/000_1_0007_1_j.png" />
</p>

## Context 
------
Computer vision is one of the fields that take more advantage of machine learning, given that programing a series of criteria to classify an image by hand is quite challenging. This is because real world images present high variability due to variables like light conditions, perspective, camera settings, signal shapes, among others. Being able to build a model from scracht and understand why does it work, is a fundamental skill for a machine learning enginerring. Therefore, we will be able to test your knowledge of the field by seeing the quality of your code and challenge your understanding of your own code. 

There are multiple methods to work with computer vision such as [neural networks](https://www.investopedia.com/terms/n/neuralnetwork.asp#:~:text=A%20neural%20network%20is%20a,organic%20or%20artificial%20in%20nature), [k-means clustering](https://en.wikipedia.org/wiki/K-means_clustering) and [support vector machines](https://en.wikipedia.org/wiki/Support-vector_machine). We strongly suggest using neural networks to solve the challenge, as we have saw better perfomance using an specific architecture of this method. However, we love seeing original approaches with good perfomance. 

## Deliverable
------
Your deliverable is a python script that must be called **model.py**, this file must have a class named Model that have a **predict(file_path)** method. The class will contain your pre-trained model, and must load an image from any size specified in the **file_path** and return an integer indicating the predicted class for that image. 

Your model can be written in pytorch, tensorflow, scikit-learn or be written entirely by you. Other libraries will not be taken into account as your model will be tested automatically. 

## Evaluation
-----
We will evaluate your code accuraccy against a larger test dataset. The accuracy will measure how many classes where identified as correct with respect to the total number of files. The **TEST** dataset use for evaluation weights around 44.4 MB compared to the one provided in the repository which size is 6,9 MB. Any code that takes longer than 15 min to evalute the entire dataset will be killed and the accuracy will be computed with the images predicted in less than 15 minutes.

This repo includes an **eval.py** script that will give an error score (lower is better). You can use it to test your
solutions against the labeled examples. We will use this script to evaluate your solution. 

We will grade solution based on the mean accuracy of the entire submissions, and gave a base score to the mean accuracy of 3. Then, your score will be computed based on how many standard deviations you're from the mean. Adding an extra point for each standard deviation above the mean, and substracting a point using the same method for scores below the mean.

Hints
------
- We have computed result with accuracies higher than 93%. You can aim to get results with this score. 
- Normalize all the images before parsing into your model, images can have different shapes.
- Use the three color channels to parse info into your model.

