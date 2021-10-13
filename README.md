# Visual question answering

## Problem definition 
We have a picture and a related question.

For example:

![10331](https://user-images.githubusercontent.com/92381157/137201546-8c937b6d-43a4-46c8-8f02-5c1e98fda089.png)

"How many people are there?"

We want to develop a software that gives the correct answer to that question:  
Output: "3"

Another example:

![10257](https://user-images.githubusercontent.com/92381157/137201832-2318bff9-5334-49df-8649-1a79a2bbb192.png)

"What is the color of the dog?"  
Output: "Yellow"

## Simplifications  
Of course, it is a very ambitious task. If the software were capable of handling any kind of picture-question, we would have basically created a human. 

To simplify the problem:
1. The possible pictures that the software can handle are simple 'cartoon' styled, as the ones just shown
2. The software can just give 58 predefined answers ('yes', 'no', 'black', 'red', '0', '1', '2', 'pie', 'plant', 'floor', ...)

Basically, it becomes a classification problem with 58 classes.

## Results
Briefly, a CNN extracts some features of the picture, a LSTM network exctacts question context. The concatenation of the features and the context is the input of a classifier, which is a Dense NN. For more details, please read "Report.pdf" and the Python notebook. For the dataset, contact me.  

The best model has a test accuracy of 58.2%



