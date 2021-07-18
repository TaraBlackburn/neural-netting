# Neural-Netting

# An investigation in learning more about how a biological neuron could aid in enhancing the artificial neural network.

[Pipeline](#Pipeline)

[Logistic Regression](#Logistic-Regression)

[Classification - K Nearest Neighboors](#Classification-K-Nearest-Neighboors)

[What I can now hypothesis](#What-I-can-now-hypothesis)

[Further Research](#Further-Research)

For the last few years I have been facinated with Neural networks in the human brain and how they can relate to our understanding of the world. There are so many subjects that can be brought together to share common knowledge to inspire one another to progress our own research and others. When I found a data set on biological neurons potential to enhance deep neural networks, I was amazed that people were already working on things that I was inspired to do. 

This dataset was used and shared (please see below for original dataset) with the anticipation that the biological neural networks could impact the understanding and computational abilities of our artifical neural networks. Here I attempt to utilized and transform this dataset to compact the findings and see if the computational abilities may embolden our advancement in artifical neural nets. 

# Pipeline
-Reading documentation on works provided
  -Trying to visualize the author’s intentions
-Researching and understanding the code
   -Changing course of action
-Importing the data from pickle files
   -7668 rows × 5 columns
-LabelEncoder for target.
   -Less columns to process (instead of one hot encoder) and still binary for my data
-Running Regressions vs Classification 

## Ran simple Machine Learning models to determine whether the dendrite is Basal vs Apical based on lengths
 
 Since Apical dendrites can be significantly longer than Basal dendrites the models were easy to train. 

I used a Logistic Regression model and KNieghborClassifer.

# Logistic Regression
**Results**

With Regression I received a 97% overall accuracy. 
Dendrite | Precision | Recall
------------ | ------------ | -------------
Apical | 100% | 96%
Basal | 94% |  99%

This Confusion Matrix is using Logisitic Regression without Cross Validation, although if you see the Precision Recall Curve below there is not a significant difference between the two regression. 

![confusion_LR](https://user-images.githubusercontent.com/61055286/126071810-f17ed2d2-cff4-4035-aaef-f2632fa154c9.png)

I assume because while a basal dendrite can stretch out from the Soma, it could reach a length where the smallest Apical dendrite may be a smililar length.

Since I did have unbalanced data, I used a Precision and Recall Curve to show the difference in the true positives and the positive predictive value for my Logisitic Regression with and without cross validation. 

![Precision Recall](https://user-images.githubusercontent.com/61055286/126071697-3db8d454-aece-4417-bbe8-1fde7b124a21.png)  

# Classification K Nearest Neighboors
Finding K with elbow curves using distortion (with Euclidean), and inertia. 

![elbow_inertia](https://user-images.githubusercontent.com/61055286/126071755-6b385a4c-49ca-4660-8e1f-2cfb56958c48.png)

![elbow_distort](https://user-images.githubusercontent.com/61055286/126071757-cb77ce1e-1186-4af1-9647-ed2643fc5022.png)

After finding my K value for the number of clusters, I fit the model and predicted my testing data. These were my results: 

![confusion_kN](https://user-images.githubusercontent.com/61055286/126071761-d220cd51-3bbe-4e3b-9553-9afde2b07f14.png)
I believe because this is a classification and my model is generally easy to classify, I was able to achieve 100% accuracy, precision and recall. 

# What I can now hypothesis
*Knowing the morphology of the cell (i.e. is it basal or apical) could potentially enhance the research of how fast the voltages from the inputs travel down the dendrites by it’s length and type. 

*What is an interesting fact is that a single pyramidal cell receives about 30,000 excitatory and 1,700 inhibitory inputs which are received in different parts of the neuron (i.e. basal vs apical)

*Excitatory inputs terminate exclusively on the dendritic spines (dense portions of the dendrite).

*Inhibitory inputs terminate on dendritic shafts, the soma, and even the axon (which as intended for outputs) this could indicate that inhibitory inputs could hold much more weight than an excitatory input, potentially even bypassing the hidden layers. 

# Further Research

*This data, from what I have seen shows the excitatory responses from NMDA, but does not mention any of the inhibitory such as GABA, but does include inhibitory synapses in the code, leading me to believe it may be unbalanced. 

*Given the information above, I believe that further research on inhibitory responses may need to be implemented as they may hold more weight in the development of outputs in a neuron (given that inhibitory inputs can terminate their voltage on an axon).

