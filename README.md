# Alzhemiers
A live demo of this project is available on [HuggingFace(Click Here)](https://huggingface.co/spaces/Pranay009/Alzheimers/tree/main).

## Dataset
---
### Context ###
The Data is hand collected from various websites with each and every labels verified.

### Content ###
The data consists of MRI images. The data has four classes of images both in training as well as a testing set:

    *Mild Demented

    *Moderate Demented

    *Non Demented

    *Very6 Mild Demented

### Dataset link ###
The Dataset can be found on [Kaggle(Click Here)](https://www.kaggle.com/datasets/tourist55/alzheimers-dataset-4-class-of-images)


## Proposed Approach 
---

The very first look on the dataset will tell you that the dataset is imbalanced and one particular class (Moderate Demented) is having very less training data and also Mild demented class is also having less data so initially i tried certain augmenting techniques like centre crop and zoom using artificial filters only for the imbalnced class but that seems to create a over fit the model while training and i realized the augmenting tecniques used to create huge variance between training data and test data same problem arise while using SMOTE finally I combined the test and the train data together and then split the data so that our model do not suffer from data variance between test and train set , I used transfer learning approach on MobileNet Architecture as we know The MobileNet Architecture uses Depth wise Convolution and The V2 version also as the skip connection which would prevent the model from overfitting as it dives into deeper layers and will keepon using features extracted in intial layers and I also reduces the computation by a good margin .

## Evaluation
---
Training accuracy: 98%
Validation accuracy:95%
Test accuracy:96%



