# Age Detection Neural Network with FASTAI

The following code is capable of predicting the age of a person. It will take an image and attempt to classify it based on eight age categories. It was implemented usign FASTAI - a deep learning library built over Pytorch. 

You can learn more about FASTAI in https://www.fast.ai/, including some amazing online, free classes that took me from zero to building this model!

## Dataset

The dataset I used is from the Adience Face Image Project - https://talhassner.github.io/home/projects/Adience/Adience-data.html#agegender. Also reference to the work by Tal Hasner et all, from the Open University of Israel - https://talhassner.github.io/home/publication/2015_CVPR

The datset contained infromation around age and gender recognition. My intend was solely around age recognition, so I stripped the gender information out of the labeling csv document that I utilized for training. 


## Implementation

I used Google Collab to train and run the algorithm, and I would recommend to do the same, should you use this for research purposes. I do provide links and further read below to try and get this to production.

### Libraries

This code uses the following libraries - 
* FASTAI
* Pytorch
* Numpy
* Pandas

As mentioned before, if you use Google Collab you should have all dependencies for training ready. If you intent to train a new model you would require a GPU which Google Collab provides. 
Do note that at the time of this post, FASTAI was having problems with the latest Pytorch version (1.5). The command below will downgrade to 1.4 - 

!pip install torch===1.4.0 torchvision===0.5.0 -f https://download.pytorch.org/whl/torch_stable.html

### Files Provided

You will find two Jupyter Notebooks - 
* age-detection-training - with all of the information required to train the model from scracth. 
* age-detection-prediction - a quick explanation about how to load the model and use it for predictions (inference).  

There are a few folders: data, with all of the data files required for model training; images, with a few free usage pictures for testing inferece; and models, which contains the exported neural net models. 

## FASTAI Neural Net Info & Results

This neural net is a resnet 50, that I trained with over 13,000 pictures provided in the dataset for about 45 epochs. I took approximately 2 hours to train usign Google Colab. 

The model's accuracy is 84.4%, which as per my research is top-of-the line. Using a "1-off" calculation (i.e. whenever the model predicts the wrong category but this is adjacent to the right one, we do not consider this a miss) the accuracy boosts to 96.6%

## References

Gil Levi and Tal Hassner.Age and Gender Classification Using Convolutional Neural Networks. IEEE Workshop on Analysis and Modeling of Faces and Gestures (AMFG), at the IEEE Conf. on Computer Vision and Pattern Recognition (CVPR), Boston, 2015. 
Link to the paper - https://talhassner.github.io/home/publication/2015_CVPR
