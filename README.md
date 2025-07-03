## Problem Statement :- 
In this work, we are finetuning a DistilBERT model on a drilling logs dataset by ONGC. The goal is to automate the process of event extraction. The input variable is the "Service hour type", which is an attribute of "text data type". The output or the vaiable to be predicted is the "Cde" or Code value, which is an Alphanumeric data type.  

### Steps followed :- 
1. Conversion of given dataset in excel format to Python dataframe object.
2. Dropping all null values.
3. Preprocessing the text of the input column, i.e, The service hours type.
4. Discarding the very rare instances of input, because keep them in the training set will lead to a class imbalance issue. ( Threshold for the number of instances is set to be 10 ).
5. Label encoding the output/target features.
6. Splitting the dataset in the ratio of 7:3. Here, I have done stratified splitting.
7. Tokenizing the train & test encodings.
8. Forming Pytorch datasets.
9. Training the model for 30 epochs.
10. Evaluating the training loss & accuracy. 
