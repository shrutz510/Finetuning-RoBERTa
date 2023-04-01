# Finetuning-RoBERTa

Requirements:

datasets 2.11.0
transformers 4.27.4

Code Description:

1) Data loading & pre-processing: 
We start by loading the AG News dataset using PyTorch. The data is tokenized using a RoBertTokenizer. The dataset is finally split into train, test, and validation datasets with a batch size 256.

2) Creating the & training the model: 
This program uses a pre-trained RoBERT Classification model with an Adam optimizer and  Cross Entropy loss function. We freeze the pre-trained RoBERTa parameters and reduce the total trainable parameters to 593668. Finally, we train the model for 3 epochs and evaluate it against the validation dataset. The model with the highest validation accuracy is saved and use to measure the accuracy of the test dataset.

3) Evaluating the results: 
This model gives the best validation accuracy of 90.61% in epoch 3 with train accuracy 87.31%, train loss 0.370, and validation loss 0.267. These results match with the expected values. The final test accuracy is 90.59% and the test loss is 0.277 which is also as expected. The model is then checked against other metrics giving the following results.
Precision: 0.906
Recall: 0.762
F1 Score: 0.828
