# Plant Pathology-2021
[Plant Pathology 2021 - FGVC8](https://www.kaggle.com/competitions/plant-pathology-2021-fgvc8/overview/description)
## Description
The main objective of the competition is to develop machine learning-based models to accurately classify a given leaf image from the test dataset to a particular disease category, and to identify an individual disease from multiple disease symptoms on a single leaf image.
## Requirements
```
conda env create -f environment.yml
```
[plant_dataset](https://pan.baidu.com/s/1VW0tQrboEhKtaURbcSJUvQ?pwd=px6v )
## File Structure
```
pythonProject1
    plant_dataset
        test
            images
            test_labels.csv
        train
            images
            train_labels.csv
        val
            images
            val_labels.csv
    main4.ipynb
    main6.ipynb
```
## models
Here, resnet18 is used to solve the classification task.    
This is a multi-class classification problem.There are 6 labels,including:
```
complex
frog_eye_leaf_spot
healthy
powdery_mildew
rust
scab
```
We use sklearn to encode the labels.
### main4.ipynb
Use a onehot encoding with a length of 6.
### main6.ipynb
Use a onehot encoding with a length of 5,where healthy is encoded as [0,0,0,0,0].
## Experimental Results
In main4.ipynb, the test accuracy is 0.7533.    
In main6.ipynb, the test accuracy is 0.805.     
The result illustrates that the second way of encoding is better.  
In fact, resnet18 is very simple and not an optimal model for this task.    
Maybe resnext,vit ,efficientnet,etc. will be better.


