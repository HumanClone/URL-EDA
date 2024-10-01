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

