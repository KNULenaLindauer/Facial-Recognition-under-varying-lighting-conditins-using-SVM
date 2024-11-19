# Facial-Recognition-under-varying-lighting-conditins-using-SVM
Project report for Understanding of Images

### Project Results and Overview
Key Objectives
This project aims to address the challenges of facial recognition under varying lighting conditions using Support Vector Machines (SVM). Lighting variations often degrade the performance of facial recognition systems by altering or obscuring key facial features. The objectives of this project are:

- To develop a robust SVM model capable of classifying facial images with high accuracy.
- To demonstrate the effectiveness of SVM in handling variations caused by changes in lighting.
- To evaluate the performance of the model on the Extended Yale B dataset, which is specifically designed for testing facial recognition under controlled lighting conditions.
Results

##### Accuracy
The model achieved a test accuracy of X% when trained and tested on distinct subsets of the dataset. This result highlights the capability of SVM to classify faces under diverse lighting conditions.
##### Performance
The SVM-based approach is computationally efficient and well-suited for small-to-medium-sized datasets, making it a viable solution for controlled environments.
#### Insights
Lighting variations significantly affect facial recognition performance, particularly under extreme lighting conditions.
Preprocessing, such as resizing and grayscale conversion, played a critical role in improving the model's accuracy by standardizing input images.
Misclassifications occurred in cases where shadows heavily distorted the facial features, indicating the need for additional preprocessing or data augmentation.
Motivation and Significance
Facial recognition is an integral technology in modern applications, from security and surveillance to biometric authentication. However, ensuring reliable performance in diverse real-world environments remains a challenge. This project addresses one of the most common environmental factors—lighting variability—by demonstrating how machine learning algorithms, specifically SVMs, can be utilized to improve recognition accuracy.

By solving this problem, the project contributes to the development of more robust facial recognition systems, potentially enhancing their application in security systems, mobile devices, and other critical areas.





### Source Code
The used Source Code has been created in Google Colab and ist listed in this repsoitory in the file order "NAME TO BE INSERTED"
The file strucrure consists of the following:
- dfv
- dfvdfv
- j

### Performance Metrices
Man klatsche die Bilder für die verschiedenen Ausgänge einmal hier herein- evtl. noch ein Vergleich zu k algo oder anderen um zu zeigen, dass Accuracy dann nicht so hoch ist (GLaubwürdigkeit und so)

### Installation and Usage
Datensatz !!!!!!!!!!!!!!


### References and Documentation
Füge Übersicht Latex File ein (also ursprünglich hochgeladenes Dokument)
- Liste der Quellen
- ...

### Issues and Contributions
One of the primary challenges observed in this project is the model's limited generalization to extreme lighting conditions. While the SVM performs well under most scenarios, it struggles when faced with very bright or heavily shadowed images, where facial features become significantly obscured or distorted. Another limitation is the relatively small size of the Extended Yale B dataset, which, despite its controlled lighting variations, does not capture real-world complexities such as facial expressions, occlusions, or diverse backgrounds.

The scalability of the model is another concern. SVMs are computationally intensive, especially when handling larger datasets, due to their quadratic training complexity. This may pose challenges for scaling the project to datasets with a significantly higher number of samples. Additionally, the model’s accuracy depends heavily on preprocessing steps such as resizing and grayscale conversion. Any inconsistencies or errors during these steps can negatively impact performance.

Contributions:
- mal schauen ob sich da noch was brauchbares finden lässr

### Future work
To build on the current project, several potential improvements can be explored. One promising direction is the incorporation of neural networks, particularly Convolutional Neural Networks (CNNs), which can provide superior performance on larger and more diverse datasets by learning hierarchical feature representations. Data augmentation is another avenue worth pursuing, as it can enrich the dataset with synthetic variations, including different lighting angles, occlusions, and facial expressions, to improve the model’s robustness.

Future iterations of this project could also focus on enabling real-time facial recognition by integrating a webcam or camera feed. This would require optimizing the SVM implementation or exploring alternative algorithms better suited for real-time performance. Another area for enhancement is the combination of SVM with feature extraction techniques such as Principal Component Analysis (PCA) or Histogram of Oriented Gradients (HOG), which could boost both accuracy and speed.

Finally, cross-domain testing on other datasets would help evaluate the model's ability to generalize beyond the Extended Yale B dataset. Adding explainability tools to visualize the SVM decision boundaries could also provide valuable insights into the model's behavior, increasing its interpretability and trustworthiness.
