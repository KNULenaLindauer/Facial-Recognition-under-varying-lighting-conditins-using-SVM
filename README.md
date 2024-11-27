# Facial-Recognition-under-varying-lighting-conditins-using-SVM
Project report for Understanding of Images

### Project Results and Overview
Key Objectives
Facial recognition systems are vital in modern applications, including security, surveillance, and biometric authentication. However, ensuring consistent performance under various environmental factors, especially lighting variations, is a persistent challenge. This project addresses this issue by employing Support Vector Machines (SVM) for robust facial recognition under varying lighting conditions.

The main objectives of this project are:
- Developing an SVM-based model capable of robust facial recognition
- Mitigating lighting variability in facial recognition using SVM
- Validating the model’s performance using the Extended Yale B dataset, specifically designed for controlled lighting variability
- Analyzing the model's performance and providing insights into its strengths and limitations in handling lighting variations
  
##### Accuracy
The model achieved a test accuracy of 99.94%, highlighting the effectiveness of SVM in handling diverse lighting conditions

##### Performance
The SVM-based approach demonstrated computational efficiency, making it suitable for small to medium-sized datasets
It is particularly effective in controlled environments, where preprocessing steps significantly enhance performance

##### Insights
- Impact of Lighting Variations:
Extreme lighting conditions can distort facial features, affecting recognition performance.
- Role of Preprocessing:
Steps like resizing and grayscale conversion significantly improved accuracy by standardizing input images.
- Limitations:
Misclassifications occurred in images with heavy shadows or extreme distortions, indicating a need for advanced preprocessing or data augmentation.
- Motivation and Significance
Facial recognition is central to security systems, biometric authentication, and mobile applications. However, real-world environments present challenges like lighting variability. This project demonstrates how machine learning algorithms, particularly SVM, can address these challenges, contributing to the development of more reliable systems.
-----------------------------------------------------------------------------------------------------
### Source Code
##### Structure


Für eine visuelle Darstellung der Projektstruktur, bei der die Ordner und Dateien korrekt hierarchisch angezeigt werden, kannst du die folgende Markdown-Syntax verwenden. Die Struktur wird mit Einrückungen und der richtigen Formatierung angezeigt, sodass du sie in deiner README.md Datei verwenden kannst.

Hier ist die angepasste Syntax:

markdown
Code kopieren
# Projektstruktur

Dies ist die grundlegende Ordnerstruktur deines Projekts. Du kannst diese nach Belieben anpassen.

MyProject/ 
├── Ordner1/ 
 │ ├── datei1.py 
 │ ├── datei2.py 
  ├── Ordner2/
  │ ├── datei1.py 
  │ ├── datei2.py 
├── datei_außen_1.py 
├── datei_außen_2.py 
└── README.md

##### Code
The used Source Code has been created in Google Colab and ist listed in this repsoitory in the file order "NAME TO BE INSERTED"
The code consists of the following:
- Importing all neccessary libraries
- Mounting Drive for Datset and preparing Dataset
- Loading Dataset
- Splitting Dataset into training and testing sets
- Training the SVM model with RBF kernel
- Test Set Predictions
- Calculate and display performance metrics for multiclass classification
  - Accuracy  
  - Classification Report
  - Confusion Matrix
  - Cohen's Kappa
- Example display of test images along with their predicted and actual labels

##### Remarks: 
- Google Account is required in order to use Colab
- Listed source code is uploaded as .ipynd file
- Dataset needs to be downloaded and uploaded to Google Drive to use given source code (ref. Installation and Usage)
- Loading the dataset and training the SVM Model takes a lot of time (approx 10-20 minutes each)
---------------------------------------------------------------------------------------------------------------------

### Performance Metrices
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
[[111   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0 115   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0 114   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0 110   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0 115   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0 109   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   1 110   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0 119   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0 151   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0 122   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0 129   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0 108   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0 122   0   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0 111   0   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0 126   0   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 113   0   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 110   0
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 120
    0   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
  110   0   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0 114   0   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0 103   0   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0 114   0   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0 128   0   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0 108   0   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0 127   0   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   1 122   0   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0 120   0]
 [  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    0   0   0   0   0   0   0   0   0 115]]
  
- Cohen's Kappa: 1.00

### Installation and Usage
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
5) Run the provided script
6) evaluate performance with metrics and visualizations
-------------------------------------------------------

[1] Athinodoros S. Georghiades, Peter N. Belhumeur, and David J. Kriegman.
“From Few to Many: Illumination Cone Models for Face Recognition under
Variable Lighting and Pose”. In: IEEE Transactions on Pattern Analysis and
Machine Intelligence 23.6 (2001), pp. 643–660. doi: 10.1109/34.927464. url:
https://doi.org/10.1109/34.927464.
[2] Guodong Guo, Stan Z. Li, and Kap Luk Chan. “Support vector machines
for face recognition”. In: Image and Vision Computing 19.9 (2001), pp. 631–
638. issn: 0262-8856. doi: https : / / doi . org / 10 . 1016 / S0262 - 8856(01 )
00046-4. url: https://www.sciencedirect.com/science/article/pii/
S0262885601000464.
[3] P. Phillips. “Support Vector Machines Applied to Face Recognition”. In: Advances
in Neural Information Processing Systems. Ed. by M. Kearns, S. Solla,
and D. Cohn. Vol. 11. MIT Press, 1998. url: https://proceedings.neurips.
cc/paper_files/paper/1998/file/a2cc63e065705fe938a4dda49092966f-
Paper.pdf.
[4] Waseem Rana et al. “Face Recognition in Different Light Conditions”. In:
SpringerLink (2022). doi: 10.1007/springerlink12345. url: https://link.
springer.com/article/10.1007/springerlink12345.
[5] Lichun Zhang et al. “Face Recognition Using Scale Invariant Feature Transform
and Support Vector Machine”. In: 2008 The 9th International Conference for
Young Computer Scientists. 2008, pp. 1766–1770. doi: 10.1109/ICYCS.2008.
481.

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
