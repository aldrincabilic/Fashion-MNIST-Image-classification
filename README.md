# Fashion-MNIST-Image-Classification

##google collab link:https://colab.research.google.com/drive/1t_Ksz8a69JX1Q17waOmKwx-ZDj87gXf7?usp=drive_link

#Questions:

###1. What is the Fashion MNIST dataset?
 
  ##Answer: The Fashion MNIST dataset is a collection of 70,000 grayscale images (28x28 pixels) showing 10 different types of clothing items like T-shirts, trousers, dresses, and shoes. It's often used to practice and test image classification models in machine learning.

###2. Why do we normalize image pixel values before training?
  
  ##Answer: We normalize pixel values (from 0–255 to 0–1) to make training faster and more stable. Large pixel values can slow down learning or cause problems during training, so scaling them helps the model learn better.
  
###3. List the layers used in the neural network and their functions.
  
  ##Answer: Flatten: Changes the 28x28 image into a single list of 784 numbers.
            Dense (128 units, ReLU): A hidden layer with 128 neurons that helps the model learn patterns.
            Dense (10 units): Output layer that gives scores for each of the 10 clothing classes.

###4. What does an epoch mean in model training?
  
  ##Answer: An epoch means the model has seen all training images once. In this case, the model was trained for 10 epochs, so it processed all 60,000 training images 10 separate times.

###5. Compare the predicted label and actual label for the first test image.
  
  ##Answer: The actual comparison result is not fully shown in the provided logs, but typically you would check if np.argmax(predictions[0]) matches test_labels[0].
            
###6. What could be done to improve the model’s accuracy?
  
  ##Answer: Add more layers or neurons
            Use a CNN (Convolutional Neural Network)
            Train for more epochs
            Use data augmentation (flip, rotate images)
            Add dropout to prevent overfitting
            Tune hyperparameters (learning rate, batch size)
            Use a validation set during training


  
      
