# Backward pass

There are two steps in the backward pass,
1. Backpropagation
2. Update the Weights and Biases According to the Gradient Descent Algorithm


### 1. Backpropagation to Determine How Much Each Weight and Bias Contributes to That Error

In the backward pass, the main goal is to compute the gradients of the loss function with respect to each weight and bias in the network. These gradients indicate how much each weight and bias contributes to the total error of the network.

The process involves applying the chain rule of calculus to propagate the error backward through the network. Starting from the output layer and moving backward through each layer, the gradients are computed layer by layer.

For a given layer, the gradient of the loss with respect to its weights and biases can be computed using the gradients from the next layer (closer to the output) and the layer's activations. The formula for computing these gradients depends on the activation function used in the layer.

### 2. Update the Weights and Biases According to the Gradient Descent Algorithm

Once the gradients with respect to the weights and biases are computed using backpropagation, the next step is to update the weights and biases to minimize the loss function.

The weights and biases are updated using a technique called gradient descent. The update rule is:

$$
\text{weight} = \text{weight} - \text{learning\_rate} \times \text{gradient}
$$

$$
\text{bias} = \text{bias} - \text{learning\_rate} \times \text{gradient}
$$

Here:
- **weight**: The weight being updated.
- **learning\_rate**: A hyperparameter that controls the step size during the update. It determines how much we are adjusting the weights in the direction of the gradient.
- **gradient**: The gradient of the loss with respect to the weight or bias.

This update rule adjusts the weights and biases in the direction that minimizes the loss function. By iteratively applying the backward pass and weight updates, the network learns to make better predictions over time.

> The backward pass in backpropagation involves computing the gradients of the loss function with respect to each weight and bias in the network and then updating these weights and biases using the gradient descent algorithm to minimize the loss.