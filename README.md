# Facial-Recognition-under-varying-lighting-conditins-using-SVM
Project report for Understanding of Images

### Project Results and Overview
Key Objectives
This project aims to address the challenges of facial recognition under varying lighting conditions using Support Vector Machines (SVM). Lighting variations often degrade the performance of facial recognition systems by altering or obscuring key facial features. The objectives of this project are:

- To develop a robust SVM model capable of classifying facial images with high accuracy.
- To demonstrate the effectiveness of SVM in handling variations caused by changes in lighting.
- To evaluate the performance of the model on the Extended Yale B dataset, which is specifically designed for testing facial recognition under controlled lighting conditions.
- Dimensions of Extended Yale Datset B: .......................(to be inserted)...................
Results:
- very high accuracy
-
-
Zusatz: entferne Warning Meldung, damit der Code später beim Testen durch Prof besser durchläuft

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
This project has been implememnted with Google Colab.   (list was Colab benötigt -Google Konto)
The choosen data set is the Extended Yale B dataset, which needs to be implemented into the environment. In this example the data has been downloaded from ...........(explain how to includde and implement the dataset (source verlinken)).

After the succesfull upload of the dataset to Google One Drive, the data can be accessed through Colab.

The program itself can then be tested and run without any further adjustions.

The Extended Yale Face Dataset B can be obtained from its official source at the following link: http://vision.ucsd.edu/extyaleb/CroppedYaleBZip/CroppedYaleB.zip. After downloading the dataset, it is necessary to extract the contents. Upon extraction, the dataset should be uploaded to Google Drive for integration into the project. The folder structure, including all subdirectories and image files, must be preserved to ensure correct file referencing.

To access the dataset within a Google Colab environment, the Google Drive must first be mounted. This can be achieved by using the following code snippet at the beginning of the Colab notebook:

from google.colab import drive
drive.mount('/content/drive')

Upon successful authentication, the dataset can be accessed by specifying the correct path to the dataset folder in the script.

dataset_path = '/content/drive/My Drive/ExtendedYaleB'

This path allows the script to access the dataset stored in Google Drive, preprocess the images by resizing them to the specified dimensions, and flatten them for feature extraction. After setting the appropriate dataset path, the script can be executed within the Colab environment. The script will automatically load, process, and train the model on the dataset, generating performance metrics such as accuracy, precision, recall, and the classification report. Additionally, visualizations, including test image predictions and, if applicable, ROC and precision-recall curves, will be produced.


### References and Documentation
Füge Übersicht Latex File ein (also ursprünglich hochgeladenes Dokument)
- Liste der Quellen
- ...

### Issues and Contributions
One of the primary challenges observed in this project is the model's limited generalization to extreme lighting conditions. While the SVM performs well under most scenarios, it struggles when faced with very bright or heavily shadowed images, where facial features become significantly obscured or distorted. Another limitation is the relatively small size of the Extended Yale B dataset, which, despite its controlled lighting variations, does not capture real-world complexities such as facial expressions, occlusions, or diverse backgrounds.

The scalability of the model is another concern. SVMs are computationally intensive, especially when handling larger datasets, due to their quadratic training complexity. This may pose challenges for scaling the project to datasets with a significantly higher number of samples. Additionally, the model’s accuracy depends heavily on preprocessing steps such as resizing and grayscale conversion. Any inconsistencies or errors during these steps can negatively impact performance.

Laden des Datasets dauert sehr lange (ca 30 Minuten) 

Contributions:
- mal schauen ob sich da noch was brauchbares finden lässr

### Future work
(Irgendwo sollt enoch angemerkt werden, dass dieser Datensatz quasi perfekt für die Aufgabe geeignet ist, da sehr viele Fotos der Individueen vorhanden sind --> quasi perfekte Trainingsbedingungen)

To build on the current project, several potential improvements can be explored. One promising direction is the incorporation of neural networks, particularly Convolutional Neural Networks (CNNs), which can provide superior performance on larger and more diverse datasets by learning hierarchical feature representations. Data augmentation is another avenue worth pursuing, as it can enrich the dataset with synthetic variations, including different lighting angles, occlusions, and facial expressions, to improve the model’s robustness.

Future iterations of this project could also focus on enabling real-time facial recognition by integrating a webcam or camera feed. This would require optimizing the SVM implementation or exploring alternative algorithms better suited for real-time performance. Another area for enhancement is the combination of SVM with feature extraction techniques such as Principal Component Analysis (PCA) or Histogram of Oriented Gradients (HOG), which could boost both accuracy and speed.

Finally, cross-domain testing on other datasets would help evaluate the model's ability to generalize beyond the Extended Yale B dataset. Adding explainability tools to visualize the SVM decision boundaries could also provide valuable insights into the model's behavior, increasing its interpretability and trustworthiness.
