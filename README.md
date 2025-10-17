# cifar10_CNNtraining_project
CNN training using Pytorch

Code block 1. Import all neccessary library from PyTorch to train CNN model

Code block 2. Import torch_directml to get AMD GPU device to train CNN model

Code block 3. Object-Oriented Programming to load dataset into Pytorch by inherit Dataset from Pytorch library
- Perform transformation for data augmentation such as horizontal flipping, random rotation 15 degree, auto-contrast to learn in different lightnining condition.
- Resize the images dataset
- Convert the images to tensor
- Normalize data

Code block 4. Split the dataset 80/20 where 80% is training data and 20% is validation data using sklearn and SubSet from Pytorch.

Code block 5. Build CNN model as Object-Oriented.
- Same CNN layer where it has convolution layer => activation layer => max pool layer.
- All the layers between the sequences are for regularization for prevent overfitting.
- Common CNN ending layers such as Flatten, Linear

Code block 6. train the data with Adam optimizer, batch_size 128, learning_rate 0.001, 30 epochs to AMD GPU and display loss every epoch. Save the model at the end of training to avoid re-train.

Before any of this turn the model to evaluation mode => cnn.eval()

Code block 7. Using validation set, evaluate Precision and Recall score for each class.

Code block 8. Using validation set, evaluate Precision and Recall score for overall weighted.

Code block 9. Using validation set, evaluate Precision and Recall score for small classes.

Code block 10. Using train and validation set, evaluate Accuracy score for both training set and validation set. Notice how they have the same score, this does not look like overfitting.

