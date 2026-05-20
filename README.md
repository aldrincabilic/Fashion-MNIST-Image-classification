# Fashion-MNIST-Image-Classification

## google collab link:https://colab.research.google.com/drive/1t_Ksz8a69JX1Q17waOmKwx-ZDj87gXf7?usp=drive_link

# Tasks Enhancement:

### 1. Change the number of neurons in the hidden layer (e.g., 64 or 256) and retrain the model.
#### Answer: A loop is used for 3 different models, each with 64, 128 (original baseline) and 256 neurons, which are all trained for 10 epochs. A comparison of their final test accuracies is done in a bar chart after training.Expected result 64 neurons will result in slightly less accuracy because of less capacity. In most cases, a small edge of 256 neurons is enough to beat 128 neurons on Fashio.


### 2. Increase the number of epochs and observe changes in accuracy.
#### Answer: Four models are trained with the original 128-neuron architecture, with 5, 10, 20, and 30 epochs. There are 2 plots generated:Training accuracy as function of epochs for each config, Validation accuracy per epochs for each config. 
Desired outcome: improvement in accuracy will be observed at 20 epochs compared to 10 epochs then compared to 5 epochs. The training accuracy continues to rise, while validation accuracy has leveled off or fallen slightly, which is indicative of overfitting.The training accuracy is still increasing while the validation accuracy is either stagnating or slightly decreasing, a typical sign of overfitting.

### 3. Add another hidden layer and compare the results.
#### Answer: They are trained for 10 epochs. A validation accuracy curve and a final bar chart are used to compare the results.The expected result: The more complex the pattern, the better the deeper the model. But on Fashion-MNIST, the gains of increasing the number of layers are small and risking overfitting takes place if there is no regularization (Dropout, BatchNorm, etc.).

#Questions:

### 1. What is the Fashion MNIST dataset?
 
  ## Answer: The Fashion MNIST dataset is a collection of 70,000 grayscale images (28x28 pixels) showing 10 different types of clothing items like T-shirts, trousers, dresses, and shoes. It's often used to practice and test image classification models in machine learning.

### . Why do we normalize image pixel values before training?
  
  ## Answer: We normalize pixel values (from 0–255 to 0–1) to make training faster and more stable. Large pixel values can slow down learning or cause problems during training, so scaling them helps the model learn better.
  
### 3. List the layers used in the neural network and their functions.
  
  ## Answer: Flatten: Changes the 28x28 image into a single list of 784 numbers.
            Dense (128 units, ReLU): A hidden layer with 128 neurons that helps the model learn patterns.
            Dense (10 units): Output layer that gives scores for each of the 10 clothing classes.

### . What does an epoch mean in model training?
  
  ## Answer: An epoch means the model has seen all training images once. In this case, the model was trained for 10 epochs, so it processed all 60,000 training images 10 separate times.

### 5. Compare the predicted label and actual label for the first test image.
  
  ## Answer: The actual comparison result is not fully shown in the provided logs, but typically you would check if np.argmax(predictions[0]) matches test_labels[0].
            
### 6. What could be done to improve the model’s accuracy?
  
  ## Answer: Add more layers or neurons
            Use a CNN (Convolutional Neural Network)
            Train for more epochs
            Use data augmentation (flip, rotate images)
            Add dropout to prevent overfitting
            Tune hyperparameters (learning rate, batch size)
            Use a validation set during training


  
      
