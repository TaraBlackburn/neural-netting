# Neural-Netting

# An investigation in learning more about how a biological neuron could aid in enhancing the artificial neural network.

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
Apical Precision - 100%, Recall - 96%
Basal Precision - 94%, Recall - 99%

See [Confusion Matrix]('../img/confusion_LR.png'). This confusion matrix is using Logisitic Regression without Cross Validation, although if you see the Precision Recall Curve below there is not a significant difference between the two regression. 

I assume because while a basal dendrite can stretch out from the Soma, it could reach a length where the smallest Apical dendrite may be a smililar length.

Since I did have unbalanced data, I used a Precision and Recall Curve to show the difference in the true positives and the positive predictive value for my Logisitic Regression with and without cross validation. 

This image shows the ![Precision and Recall]('img/precision_recall.png') Curve. 



# What I can now hypothesis
Knowing the morphology of the cell (i.e. is it basal or apical) could potentially enhance the research of how fast the voltages from the inputs travel down the dendrites by it’s length and type. 
What is an interesting fact is that a single pyramidal cell receives about 30,000 excitatory and 1,700 inhibitory inputs which are received in different parts of the neuron (i.e. basal vs apical)
Excitatory inputs terminate exclusively on the dendritic spines (dense portions of the dendrite).
Inhibitory inputs terminate on dendritic shafts, the soma, and even the axon (which as intended for outputs) this could indicate that inhibitory inputs could hold much more weight than an excitatory input, potentially even bypassing the hidden layers. 
