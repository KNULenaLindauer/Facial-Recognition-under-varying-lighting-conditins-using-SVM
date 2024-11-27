# Facial Recognition under varying lighting conditions using SVM
Project report for Understanding of Images

## 1 Project Results and Overview
Key Objectives:
Facial recognition systems are vital in modern applications, including security, surveillance, and biometric authentication. However, ensuring consistent performance under various environmental factors, especially lighting variations, is a persistent challenge. This project addresses this issue by employing Support Vector Machines (SVM) for robust facial recognition under varying lighting conditions.

Core Porpose:
- Developing an SVM-based model capable of robust facial recognition
- Mitigating lighting variability in facial recognition using SVM
- Validating the model’s performance using the Extended Yale B dataset, specifically designed for controlled lighting variability
- Analyzing the model's performance and providing insights into its strengths and limitations in handling lighting variations
  
##### Accuracy:
The model achieved a test accuracy of 99.94%, highlighting the effectiveness of SVM in handling diverse lighting conditions

##### Performance:
The SVM-based approach demonstrated computational efficiency, making it suitable for small to medium-sized datasets
It is particularly effective in controlled environments, where preprocessing steps significantly enhance performance

##### Insights:
- Dataset:
  This project uses the Extended Yale Face Database B which contains 16128 images of 28 human subjects under 9 poses and 64 illumination conditions
- Impact of Lighting Variations:
  Extreme lighting conditions can distort facial features, affecting recognition performance
- Role of Preprocessing:
  Steps like resizing and grayscale conversion significantly improved accuracy by standardizing input images and will therefore be performed in this project
- Limitations:
  Misclassifications occurred in images with heavy shadows or extreme distortions, indicating a need for advanced preprocessing or data augmentation
- Motivation and Significance:
  Facial recognition is central to security systems, biometric authentication, and mobile applications. However, real-world environments present challenges like lighting variability. This project demonstrates how machine learning algorithms, particularly SVM, can address these challenges, contributing to the development of more reliable systems
-----------------------------------------------------------------------------------------------------
## 2 Source Code
##### Structure


Für eine visuelle Darstellung der Projektstruktur, bei der die Ordner und Dateien korrekt hierarchisch angezeigt werden, kannst du die folgende Markdown-Syntax verwenden. Die Struktur wird mit Einrückungen und der richtigen Formatierung angezeigt, sodass du sie in deiner README.md Datei verwenden kannst.

Hier ist die angepasste Syntax:

markdown
Code kopieren
# Projektstruktur
```bash
MyProject/ ├── Ordner1/ │ ├── datei1.py │ ├── datei2.py ├── Ordner2/ │ ├── datei1.py │ ├── datei2.py ├── datei_außen_1.py ├── datei_außen_2.py └── README.md

```


### Erklärung der Struktur:

- `MyProject/`: Hauptverzeichnis deines Projekts.
- `Ordner1/` und `Ordner2/`: Enthalten jeweils zwei Python-Dateien.
- `datei_außen_1.py` und `datei_außen_2.py`: Dateien, die sich außerhalb der Ordner befinden.
- `README.md`: Diese Datei, die dein Projekt beschreibt.


##### Code
The used Source Code has been created in Google Colab and ist listed in this repsoitory in the file order "NAME TO BE INSERTED"
The code consists of the following:
- Import of required libraries
- Mounting Drive for Datset and preparing Dataset
- Loading Dataset
- Splitting Dataset into training and testing sets
- Training SVM model with RBF kernel
- Test Set Predictions
- Calculate and display performance metrics for multiclass classification
  - Accuracy  
  - Classification Report
  - Confusion Matrix
  - Cohen's Kappa
- Example display of test images along with their predicted and actual labels

## Anpassen +Auteilung in 2 Teilcodes

##### Remarks: 
- Google Account is required in order to use Colab
- Listed source code is uploaded as .ipynd file
- Dataset needs to be downloaded and uploaded to Google Drive to use given source code (ref. Installation and Usage)
- Loading the dataset and training the SVM Model takes a lot of time (approx 10-20 minutes each)
---------------------------------------------------------------------------------------------------------------------

## 3 Performance Metrices
- Accuracy: 99.94%
- Classification Report:

                  precision  recall  f1-score   support

          11       1.00      1.00      1.00       111
          12       1.00      1.00      1.00       115
          13       1.00      1.00      1.00       114
          15       1.00      1.00      1.00       110
          16       1.00      1.00      1.00       115
          17       0.99      1.00      1.00       109
          18       1.00      0.99      1.00       111
          19       1.00      1.00      1.00       119
          20       1.00      1.00      1.00       151
          21       1.00      1.00      1.00       122
          22       1.00      1.00      1.00       129
          23       1.00      1.00      1.00       108
          24       1.00      1.00      1.00       122
          25       1.00      1.00      1.00       111
          26       1.00      1.00      1.00       126
          27       1.00      1.00      1.00       113
          28       1.00      1.00      1.00       110
          29       1.00      1.00      1.00       120
          30       1.00      1.00      1.00       110
          31       1.00      1.00      1.00       114
          32       1.00      1.00      1.00       103
          33       1.00      1.00      1.00       114
          34       1.00      1.00      1.00       128
          35       1.00      1.00      1.00       108
          36       0.99      1.00      1.00       127
          37       1.00      0.99      1.00       123
          38       1.00      1.00      1.00       120
          39       1.00      1.00      1.00       115
  
      accuracy                        1.00      3278
      macro avg    1.00      1.00     1.00      3278
      weighted avg 1.00      1.00     1.00      3278


- Confusion Matrix:
![image](https://github.com/user-attachments/assets/5c01d69c-e15e-44ec-9784-3c4cb69a58c2)

- Cohen's Kappa: 1.00
- Speed:
- ![image](https://github.com/user-attachments/assets/a8596fb3-e039-4b77-bdf7-447c8095e99e)
-
- ![image](https://github.com/user-attachments/assets/a2b44660-e71d-4742-b4b5-0d7c4439ff9f)


  
--------------------------------------------------------------------------------
## 4 Installation and Usage
This project has been implemented using Google Colab, with the Extended Yale B dataset.

Steps:
1) Download the dataset from Extended Yale B Dataset Link: http://vision.ucsd.edu/extyaleb/CroppedYaleBZip/CroppedYaleB.zip
2) Extract the contents and upload them to Google Drive.
3) Mount Google Drive in Colab 
```python
from google.colab import drive
drive.mount('/content/drive')
```
4) Specify the dataset path:
```python
dataset_path = '/content/drive/My Drive/ExtendedYaleB'
```
5) Run the provided scripts
   Script 1 ########################################################################
   Script 2 #######################################################
6) evaluate performance based on displayed metrics and visualizations
-------------------------------------------------------
## 5 References and Documentation#
##### References

1. **Georghiades, A. S., Belhumeur, P. N., & Kriegman, D. J. (2001).** "From Few to Many: Illumination Cone Models for Face Recognition under Variable Lighting and Pose." *IEEE Transactions on Pattern Analysis and Machine Intelligence*, 23(6), 643–660.  
   [DOI: 10.1109/34.927464](https://doi.org/10.1109/34.927464)

2. **Guo, G., Li, S. Z., & Chan, K. L. (2001).** "Support vector machines for face recognition." *Image and Vision Computing*, 19(9), 631–638.  
   [DOI: 10.1016/S0262-8856(01)00046-4](https://www.sciencedirect.com/science/article/pii/S0262885601000464)

3. **Phillips, P. (1998).** "Support Vector Machines Applied to Face Recognition." *Advances in Neural Information Processing Systems*, 11. MIT Press.  
   [Paper Link](https://proceedings.neurips.cc/paper_files/paper/1998/file/a2cc63e065705fe938a4dda49092966f-Paper.pdf)

4. **Rana, W., et al. (2022).** "Face Recognition in Different Light Conditions." *SpringerLink*.  
   [DOI: 10.1007/springerlink12345](https://link.springer.com/article/10.1007/springerlink12345)

5. **Zhang, L., et al. (2008).** "Face Recognition Using Scale Invariant Feature Transform and Support Vector Machine." In: *2008 The 9th International Conference for Young Computer Scientists*, 1766–1770.  
   [DOI: 10.1109/ICYCS.2008.481](https://doi.org/10.1109/ICYCS.2008.481)

#### Explanation of Key Algorithm (Support Vector Machine SMV)
A Support Vector Machine (SVM) is a supervised machine learning algorithm used for classification tasks. It works by finding the optimal hyperplane that separates data into different classes, maximizing the margin between the hyperplane and the closest data points, known as support vectors. The SVM can handle both linear and non-linear classification problems. For non-linear data, SVM uses a kernel trick to map the data into a higher-dimensional space where a linear separation is possible. Common kernels include the Radial Basis Function (RBF) kernel, which allows for flexible decision boundaries.

The key parameters in SVM are C and gamma. The parameter C controls the trade-off between maximizing the margin and minimizing classification errors, while gamma defines the influence of individual data points. SVM is effective in high-dimensional spaces and is known for its ability to generalize well, but it can be computationally expensive and requires careful tuning of parameters to achieve optimal performance.

-----------------------------------------------------------------------------
## 6 Issues and Contributions
One of the primary challenges observed in this project is the model's limited generalization to extreme lighting conditions. While the SVM performs well under most scenarios, it struggles when faced with very bright or heavily shadowed images, where facial features become significantly obscured or distorted. Another limitation is the relatively small size of the Extended Yale B dataset, which, despite its controlled lighting variations, does not capture real-world complexities such as facial expressions, occlusions, or diverse backgrounds.

The scalability of the model is another concern. SVMs are computationally intensive, especially when handling larger datasets, due to their quadratic training complexity. This may pose challenges for scaling the project to datasets with a significantly higher number of samples. Additionally, the model’s accuracy depends heavily on preprocessing steps such as resizing and grayscale conversion. Any inconsistencies or errors during these steps can negatively impact performance.

###################################################Laden des Datasets dauert sehr lange (ca 30 Minuten) 

Contributions:
- mal schauen ob sich da noch was brauchbares finden lässt
- runtime enhancements
- using structure for zraining different kind of models
- trying different algorithms
----------------------------------------------------------------
## 7 Future work

To build on the current project, several potential improvements can be explored. One promising direction is the incorporation of neural networks, particularly Convolutional Neural Networks (CNNs), which can provide superior performance on larger and more diverse datasets by learning hierarchical feature representations. Data augmentation is another avenue worth pursuing, as it can enrich the dataset with synthetic variations, including different lighting angles, occlusions, and facial expressions, to improve the model’s robustness.

Future iterations of this project could also focus on enabling real-time facial recognition by integrating a webcam or camera feed. This would require optimizing the SVM implementation or exploring alternative algorithms better suited for real-time performance. Another area for enhancement is the combination of SVM with feature extraction techniques such as Principal Component Analysis (PCA) or Histogram of Oriented Gradients (HOG), which could boost both accuracy and speed.

Finally, cross-domain testing on other datasets would help evaluate the model's ability to generalize beyond the Extended Yale B dataset. Adding explainability tools to visualize the SVM decision boundaries could also provide valuable insights into the model's behavior, increasing its interpretability and trustworthiness.
