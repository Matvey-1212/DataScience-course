# Determining a person's age from a photo

The project involves analyzing data consisting of photographs of people's faces along with their age information. Using this data, a convolutional neural network (CNN) based on ResNet50 architecture is trained to predict the age of individuals from a given photograph.

**Project Summary:**

In this project, a dataset consisting of 7591 images in the format (256, 256, 3) with age information was utilized. Augmentation techniques were applied, including RGB normalization to [0-1], rotation up to 20 degrees, scaling down to 20%, horizontal reflection, and brightness adjustment in the range [0.7-1.3].

A model based on the ResNet50 architecture was employed to predict the age of individuals from images. This model was pretrained on ImageNet, with the final layer replaced by dropout, Global Average Pooling (GAP), a fully connected layer with 512 neurons and ReLU activation, and a final fully connected layer with one neuron and ReLU activation.

The training process was conducted using the Adam optimizer with a learning rate of 0.0003 and Mean Squared Error (MSE) as the loss function. Mean Absolute Error (MAE) was used as the quality metric.

**Final MAE after 20 epochs:**

- Train - 4.2617
- Test - 6.3242

The model did not overfit and performed adequately. An MAE of 6.3242 can be considered reasonable when compared to the result of 5.4 in the referenced [paper](https://people.ee.ethz.ch/~timofter/publications/Agustsson-FG-2017.pdf).

To improve the results, one could explore architecture modifications, such as increasing the number of convolutional and fully connected layers. However, this may lead to overfitting, necessitating hyperparameter tuning, e.g., dropout rates and the number of training epochs. Augmenting the training dataset with more data can also enhance generalization.

Another strategy to improve performance is active learning. The model's performance on the training dataset can be assessed, and examples where the model makes the most mistakes can be identified. By applying various augmentations to the training set (without fine-tuning), examples that yield the most diverse results from the model can be selected. These selected examples can help identify areas where the model struggles and guide further improvements.
