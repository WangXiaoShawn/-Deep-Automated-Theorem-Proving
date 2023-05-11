
# Predicting One-step Proofs in Formal Mathematics using Transformer-based Neural Networks
## Deep Automated Theorem Proving

**Xiao Wang** | xwang99@syr.edu   

This project aims to investigate the potential of transformer models in mathematical proof verifica-
tion, address the challenges associated with utilizing transformer models in the field of mathematics,
and provide insights into the methodology and techniques employed in developing the transformer
model for Set.mm. And our models are built based on the transformer model developed by our instructor
(Katz, [2023](https://colab.research.google.com/drive/1hIwuwZelSsSbqgJDsHJv2-peAx9wO4AL?usp=sharing)).

### Preparation
The model is built with PyTorch, so we need to make sure the environment is built up sucessfully, here is a link about PyTorch: https://pytorch.org/docs/stable/index.html

After that, we would need to get all the packages prepared by running the following code:

```python
import matplotlib.pyplot as pt
import numpy as np
import torch as tr
import random
import requests
import math
import torch.nn.functional as F
```

Here are all the packages we would need for the model, if the package is not able to import, try install it first, here is a link about how to install python package: https://packaging.python.org/en/latest/tutorials/installing-packages/

Before we run the model, we would need to get the data prepare. 

```python
!wget https://github.com/metamath/set.mm/raw/develop/set.mm
```

After runnning this code, we would have the dataset in our local environment.

### Model
We build two models for this project and each of them is a seq2seq architecure Transformer. Here are the structure of the two models:

#### Architecture1:

<p align="center">
  <img width="460" height="440" src="https://user-images.githubusercontent.com/39479326/236593734-08e2dba3-f756-455b-b554-4d740b0a0a57.png">
</p>


#### Architecture2:

<p align="center">
  <img width="460" height="440" src="https://user-images.githubusercontent.com/39479326/236641013-a31c05fd-b457-4d3d-8216-9ee3bc012376.png">
</p>

With all the preparation steps get ready, we can run the code as these two workflow shown. And here are some sample of the output:

#### A glance at the prediction for each step:

<p align="center">
  <img width="800" src="https://user-images.githubusercontent.com/39479326/236565473-61032834-93e0-4dd3-a393-25bda158bac4.png">
</p>

#### The overall model performance (plots):

<p align="center">
  <img width="460" height="440" src="https://user-images.githubusercontent.com/39479326/236641211-c8a3d05c-ebea-4d3a-a516-67dbb37acb55.png">
</p>

#### The overall model performance (avg accuracy):

<p align="center">
  <img width="460" src="https://user-images.githubusercontent.com/39479326/236593265-dab9afc5-3c38-451d-a598-4fee0f8d8475.png">

</p>

#### Model evaluation:

<p align="center">
  <img width="800" src="https://user-images.githubusercontent.com/39479326/236565360-bf03a6b8-23c1-42d9-86a7-98159e6a8d4e.png">
</p>

