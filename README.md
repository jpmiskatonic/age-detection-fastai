# Age Detection Neural Network with FASTAI

The following code is capable of predicting the age of a person. It will take an image and attempt to classify it based on eight age categories. It was implemented usign FASTAI - a deep learning library built over Pytorch. 

## Dataset
The dataset I used is from the Adience Face Image Project - https://talhassner.github.io/home/projects/Adience/Adience-data.html#agegender
In addition, the following paper also resulted an excellent read and baseline to understand the dataset -Gil Levi and Tal Hassner.Age and Gender Classification Using Convolutional Neural Networks. IEEE Workshop on Analysis and Modeling of Faces and Gestures (AMFG), at the IEEE Conf. on Computer Vision and Pattern Recognition (CVPR), Boston, 2015. 
Link to the paper - https://talhassner.github.io/home/publication/2015_CVPR

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

