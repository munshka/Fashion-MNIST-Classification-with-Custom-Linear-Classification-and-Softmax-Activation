# Fashion MNIST Classification with Custom Linear Classification and Softmax Activation

This project uses custom code for classifying images from the Fashion MNIST dataset using a linear classification approach with softmax activation. Here's a brief overview of the code and its functionalities:

## Code Explanation

1. **Data Preparation**:
   - The code starts by preparing the Fashion MNIST dataset. It flattens the input images to a 1D vector, normalizes the pixel values by dividing by 255, and calculates the number of examples and pixels.

2. **Initialization**:
   - It initializes the number of classes (in this case, 10, corresponding to different fashion items).
   - Sets up the weight matrix `W` with random values and initializes the bias vector `b` to zeros.

3. **Prediction (Scoring)**:
   - The `scored` function computes the scores for each class for each example. It uses the dot product of the flattened input data `train_X_flattened` with the weight matrix `W` and adds the bias vector `b`.
   
4. **Softmax Activation**:
   - The `softmax` function applies the softmax activation to the computed scores. Softmax converts raw scores into class probabilities. It exponentiates each score and normalizes them across classes for each example.

5. **Training**:
   - The code then enters a training loop (1000 iterations in this example).
   - In each iteration, it calculates the scores and predicted probabilities.
   - It updates the weight matrix `W` and bias vector `b` based on the gradient descent optimization. The learning rate is controlled by `lamda` (0.9 in this case).
   - The code uses the cross-entropy loss with a regularization term (not shown in the code but common in practice) to update the weights and bias.

6. **Printing Results**:
   - After training, the code prints the learned weight matrix `W` and bias vector `b`. These represent the model's learned parameters after training on the Fashion MNIST dataset.

