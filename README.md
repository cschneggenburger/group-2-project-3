**WORKING ITEMS**  
Cody - Get a working model trained on specified animals  
Dylan - get animal data set uploaded  
Shan - find example pictures to use to predict with the model. - ex. Trail cams   

# AI-project-3
This repo will be used for project 3 of the AI Bootcamp.
### Issue
Livestock and domestic animals are falling victim to attacks by predators like coyotes, foxes, and other predatory species.

### Objective
To develop an alert system that employs computer vision technology to detect predators such as coyotes and foxes, and promptly notify the owners. This system aims to protect livestock and pets from potential threats.


## Background: Livestock Predation 

- Predation accounts for the majority of livestock losses in agriculture.
- According to the U.S. Department of Agriculture’s (USDA) National Agricultural Statistics Service (NASS) in 2006:
  - Predators accounted for a loss of **190,000 head of cattle**.
  - This amounted to a monetary loss of **92.7 million dollars**.
- In California:
  - In 2015, just **1%** of reported death losses of mature cattle were attributed to predators.
  - In 2014, **19%** of reported death losses in mature sheep were caused by predators.
  - Approximately **6%** of reported calf losses in 2015 were due to predators.
  - Over **45%** of lamb losses were predator-caused.
- Only **220,000 cattle losses** stemmed from livestock predators or **0.23%** of the total cattle production over the year.

Predators include animals such as coyotes, wolves, foxes, mountain lions, grizzlies, and eagles. They play vital roles in our ecosystems but can pose challenges for ranching operations. Various strategies are used to manage livestock predation, including modifications of animal husbandry practices and habitat, population management, and novel approaches developed through research.


# Technologies Used 

### Models 

Pytorch Model - CNN  resnetpt

### Graphical User Interface
Gradio https://www.gradio.app/ 

### Dependencises for Keras Model
import keras,os  
from keras.models import Sequential  
from keras.layers import Dense, Conv2D, MaxPool2D , Flatten  
from keras.preprocessing.image import ImageDataGenerator  
import numpy as np  


### Dependencies for Pytorch Model
import torch  
from torch.utils.data import DataLoader, random_split  
from torchvision import datasets, transforms  
import torch.nn as nn  
import torch.optim as optim  
import torch.nn.functional as F  
from torchvision.models import resnet18, ResNet18_Weights #pretrained model  

## Data Sets  
https://www.kaggle.com/datasets/iamsouravbanerjee/animal-image-dataset-90-different-animals 

Future Developments


Animals Model Trained on:   

bison,  
boar,  
cow,  
coyote,
Deer,
dog,  
donkey,  
ducks,  
fox,  
goat,   
goose,   
hare,   
hedgehog,   
horse,  
mouse,  
owl,  
ox,  
pig,  
possum,  
raccoon,  
rat, 
snake,   
squirrel,  
turkey,  
wolf


Animal Classes  
animal_classes = ['cat', 'cow', 'coyote', 'deer', 'dog', 'donkey', 'fox', 'horse', 'owl', 'pig', 'possum', 'raccoon', 'sheep', 'wolf']  

# Define predator mapping (0: nonpredator, 1: predator, 2: both)
predator_mapping = {'cat': 2, 'cow': 0, 'coyote': 1, 'deer': 2, 'dog': 2, 'donkey': 0, 'fox': 1, 'horse': 0, 'owl': 1, 'pig': 0, 'possum': 1,
                    'raccoon': 1, 'sheep': 0, 'wolf': 1}
predator_classes = ['nonpredator', 'predator', 'both']


**Presentation**

Notes 

Used fine tuning on Restnet to get feature selection from pretrained model.   
Base Data Set  
Model trained on 60 images per class 14 classes.   



