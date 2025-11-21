# Brain Tumor Classification Models: Comparative Analysis

This document summarizes the performance of three different Convolutional Neural Network (CNN) models trained for brain tumor classification into four categories: `glioma`, `meningioma`, `notumor`, and `pituitary`.

## Models Evaluated

1.  **SimpleCNN**: A custom-built lightweight CNN architecture.
2.  **MobileNetV3-Small**: A pre-trained MobileNetV3-Small model fine-tuned for the task.
3.  **EfficientNet-B0**: A pre-trained EfficientNet-B0 model fine-tuned for the task.

All models were trained for 30 epochs with consistent hyperparameters (learning rate, batch size, etc.) and mixed-precision training for efficiency.

## Summary of Test Accuracies

After training and evaluation on a dedicated test set, the models achieved the following accuracies:

*   **SimpleCNN**: **95.65%**
*   **MobileNetV3-Small**: **98.86%**
*   **EfficientNet-B0**: **99.47%**

**EfficientNet-B0** demonstrated the highest performance among the three evaluated models on the given dataset.

## Evaluation Metrics and Visualizations

For each model, the following evaluation artifacts were generated:

*   **Epoch-wise Training Progress**: Logs showing training and validation loss/accuracy across all epochs, as well as the learning rate schedule. These can be explored in detail using TensorBoard.

*   **Classification Report**: Provides detailed performance metrics for each class, including:
    *   **Precision**: The proportion of correctly identified positive cases among all cases predicted as positive.
    *   **Recall**: The proportion of correctly identified positive cases among all actual positive cases.
    *   **F1-Score**: The harmonic mean of precision and recall, offering a balance between the two.
    *   **Support**: The number of actual occurrences of each class in the test set.

*   **Confusion Matrix**: A tabular visualization that allows for the performance of an algorithm to be seen visually. Each row of the matrix represents the instances in an actual class, while each column represents the instances in a predicted class.

    ### SimpleCNN Confusion Matrix
<img width="513" height="470" alt="image" src="https://github.com/user-attachments/assets/7ba89012-a075-42d6-9d81-b3da95334227" />

   ### MobileNetV3-Small Confusion Matrix
<img width="513" height="470" alt="image" src="https://github.com/user-attachments/assets/c3be39dd-b07a-42d8-a174-ae7b2796ec56" />

   ### EfficientNet-B0 Confusion Matrix
<img width="513" height="470" alt="image" src="https://github.com/user-attachments/assets/1fb7cfc4-c1fc-46da-8643-c3ef11849a16" />

*   **Grad-CAM Visualizations**: Gradient-weighted Class Activation Mapping (Grad-CAM) images highlight the regions of an input image that were most important for the model's classification decision. These are crucial for understanding model interpretability and ensuring that the model is focusing on relevant features.

    ### SimpleCNN Grad-CAM Examples
    <img width="948" height="1064" alt="download (3)" src="https://github.com/user-attachments/assets/b3e224a2-a2a6-47d6-afd4-c1958486986b" />


    ### MobileNetV3-Small Grad-CAM Examples
    <img width="948" height="1064" alt="download" src="https://github.com/user-attachments/assets/665209ea-d3bc-4167-b03c-219300960504" />


    ### EfficientNet-B0 Grad-CAM Examples
    <img width="948" height="1064" alt="download (1)" src="https://github.com/user-attachments/assets/bc1b76a4-d483-49c7-a8ba-08c6e9e46109" />




