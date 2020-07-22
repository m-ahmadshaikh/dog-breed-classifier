# Dog-Breed-Classifier
n this project, I have built a pipeline that can be used within a web or mobile app to process real-world, user-supplied images. Given an image of a dog, your algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.



## Prerequisites
1. The Code is written in **Python 3.6.5** . If you don't have Python installed you can find it [here](https://www.python.org/downloads/).
Ensure you have the latest version of pip.
2. Additional Packages that are required are: [Numpy](http://www.numpy.org/), [Pandas](https://pandas.pydata.org/), [MatplotLib](https://matplotlib.org/), [Pytorch](https://pytorch.org/), PIL and json. You can donwload them using [pip](https://pypi.org/project/pip/):
    - ```pip install numpy pandas matplotlib pil```<br/>
    or [conda](http://www.numpy.org/)
    - ```conda install numpy pandas matplotlib pil```
    
**NOTE**: In order to install Pytorch follow the instructions given on the official site.


## Data
This project would require two datasets 
One is [dog-dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip)
Second is [human-dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip)
## GPU/CPU
As this project uses deep CNNs, for training of network you need to use a GPU. However after training you can always use normal CPU for the prediction phase.

## Hyperparameters
As you can see you have a wide selection of hyperparameters available and you can get even more by making small modifications to the code. Thus it may seem overly complicated to choose the right ones especially if the training needs at least 15 minutes to be completed. So here are some hints:

- By increasing the number of epochs the accuracy of the network on the training set gets better and better but its timing consuming and saturates at higher levels.
- A big learning rate guarantees that the network will converge fast to a small error but it will constantly overshot
- A small learning rate guarantees that the network will reach greater accuracies but the learning process will take longer
- Densenet121 works best for images but the training process takes significantly longer than alexnet or vgg16

Current settings:<br/>
- lr: 0.001
- dropout: 0.3
- epochs: 15
# Transfer Learning Used:
I have used vgg11 (pretrained) model for training. I have trained on 10 epoch got an accuracy of 84% on test dataset. Feel free to choose other pretrained models.
