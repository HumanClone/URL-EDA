## Before Scaling the data but with Regularization
### Parameters
training size of 0.2
dimensionality of 16
Embedding of d(421218)
dropout at 0.2
l1 and l2 at 0.1

### Results
LSTM:accuracy: 0.9285 - loss: 0.1681 - precision: 0.9253 - recall: 0.9423 - val_accuracy: 0.9576 - val_loss: 0.1035 - val_precision: 0.9597 - val_recall: 0.9610| Epoch 1

CNN: accuracy: 0.9416 - loss: 0.1399 - precision: 0.9371 - recall: 0.9548 - val_accuracy: 0.9633 - val_loss: 0.0907 - val_precision: 0.9648 - val_recall: 0.9666| Epoch 1

RF had 95, seems to be the limit and constant 
SVM Linear had about 56
SGD had 47

## Regularization and No Scaling
### Parameters
training size of 0.2
dimensionality of 16
Embedding of d(421218)
dropout at 0.2
l1 and l2 at 0.1

### Results
LSTM:accuracy: 0.9311 - loss: 0.1726 - precision: 0.9273 - recall: 0.9452 - val_accuracy: 0.9586 - val_loss: 0.1074 - val_precision: 0.9567 - val_recall: 0.9662| epoch 1

CNN: accuracy: 0.9395 - loss: 0.1566 - precision: 0.9343 - recall: 0.9541 - val_accuracy: 0.9607 - val_loss: 0.1044 - val_precision: 0.9632 - val_recall: 0.9632|epoch 1

SVM and SGD improved 75 

## Scaling and Regularization
### Parameters
scaled the data using standardization
training size of 0.2
dimensionality of 16
Embedding of d(421218)
dropout at 0.2
l1 and l2 at 0.1

### Results
LSTM:accuracy: 0.8807 - loss: 0.2991 - precision: 0.8486 - recall: 0.9456 - val_accuracy: 0.8813 - val_loss: 0.2985 - val_precision: 0.8488 - val_recall: 0.9465| epoch 17

CNN:accuracy: 0.8725 - loss: 0.3192 - precision: 0.8414 - recall: 0.9384 - val_accuracy: 0.8769 - val_loss: 0.3112 - val_precision: 0.8451 - val_recall: 0.9423 |epoch 7 

SVM and SGD improved 75 


## Scaling and no regularization
### Parameters
scaled the data using standardization
training size of 0.25
dimensionality of 16
Embedding of d(421218)
dropout at 0.2

### Results
LSTM: accuracy: 0.8808 - loss: 0.2968 - precision: 0.8487 - recall: 0.9456 - val_accuracy: 0.8809 - val_loss: 0.2985 - val_precision: 0.8465 - val_recall: 0.9494| epoch 14 

CNN:accuracy: 0.8780 - loss: 0.3046 - precision: 0.8469 - recall: 0.9421 - val_accuracy: 0.8806 - val_loss: 0.3001 - val_precision: 0.8482 - val_recall: 0.9461|epoch 20

SVM and SGD 75


# Reformating data to have a binary for subdomain, going to compare, this with Vectorising
## Scaling and no regularization 
### Results
                precision    recall  f1-score
RF:        0       0.95      0.94      0.95     
           1       0.95      0.96      0.95
accuracy 0.95

SVC        0       0.79      0.63      0.70     
           1       0.73      0.85      0.78
accuracy 0.75

SDG        0       0.82      0.58      0.68     
           1       0.71      0.89      0.79
accuracy 0.74

LSTM:accuracy: 0.8811 - loss: 0.2928 - precision: 0.8480 - recall: 0.9476 - val_accuracy: 0.8812 - val_loss: 0.2942 - val_precision: 0.8471 - val_recall: 0.9492 |Epoch 19

CNN: accuracy: 0.8772 - loss: 0.3027 - precision: 0.8459 - recall: 0.9418 - val_accuracy: 0.8795 - val_loss: 0.2978 - val_precision: 0.8444 - val_recall: 0.9496| Epoch 13



## tdif vectorization 

dimensions (n,14,19)


### Results
                precision    recall  f1-score
RF:        0       0.96      0.90      0.93     
           1       0.91      0.97      0.94
accuracy 0.93

SVC        0       0.84      0.78      0.81     
           1       0.82      0.87      0.85 
accuracy 0.83

SDG        0       0.85      0.78      0.81     
           1       0.82      0.88      0.85
accuracy 0.83

LSTM: accuracy: 0.9337 - loss: 0.1672 - precision: 0.9248 - recall: 0.9534 - val_accuracy: 0.9317 - val_loss: 0.1720 - val_precision: 0.9195 - val_recall: 0.9559| Epoch 8

CNN:accuracy: 0.9307 - loss: 0.1787 - precision: 0.9213 - recall: 0.9517 - val_accuracy: 0.9316 - val_loss: 0.1754 - val_precision: 0.9206 - val_recall: 0.9543| epoch 30
accuracy: 0.9366 - loss: 0.1595 - precision: 0.9276 - recall: 0.9561 - val_accuracy: 0.9349 - val_loss: 0.1645 - val_precision: 0.9256 - val_recall: 0.9550 |Epoch 29

