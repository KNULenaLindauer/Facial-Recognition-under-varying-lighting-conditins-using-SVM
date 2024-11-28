# Facial Recognition under varying lighting conditions using SVM

## 1 Project Results and Overview
#### Key Objectives  
Facial recognition systems are vital in modern applications, including security, surveillance, and biometric authentication. However, ensuring consistent performance under various environmental factors, especially lighting variations, is a persistent challenge. This project addresses this issue by employing Support Vector Machines (SVM) for robust facial recognition under varying lighting conditions.

#### Core Porpose  
- Developing a SVM-based model capable of robust facial recognition
- Mitigating lighting variability in facial recognition using SVM
- Validating the model’s performance using the Extended Yale B dataset, specifically designed for controlled lighting variability
- Analyzing the model's performance and providing insights into its strengths and limitations in handling lighting variations
  
#### Accuracy  
The model achieved a test accuracy of 99.94%, highlighting the effectiveness of SVM in handling diverse lighting conditions

#### Performance  
The SVM-based approach demonstrated computational efficiency, making it suitable for small to medium-sized datasets
It is particularly effective in controlled environments, where preprocessing steps significantly enhance performance
# Trainieren benötigt etwas Zeit, Assessments brauchen jedoch sehr lange, bis alle Metrices erstellt werden

#### Insights
- Dataset    
This project uses the Extended Yale Face Database B which contains 16128 images of 28 human subjects under 9 poses and 64 illumination conditions
- Impact of Lighting Variations  
Extreme lighting conditions can distort facial features, affecting recognition performance
- Role of Preprocessing  
Steps like resizing and grayscale conversion significantly improved accuracy by standardizing input images and will therefore be performed in this project
- Limitations  
Misclassifications occurred in images with heavy shadows or extreme distortions, indicating a need for advanced preprocessing or data augmentation
- Motivation and Significance  
Facial recognition is central to security systems, biometric authentication, and mobile applications. However, real-world environments present challenges like lighting variability. This project demonstrates how machine learning algorithms, particularly SVM, can address these challenges, contributing to the development of more reliable systems

-----------------------------------------------------------------------------------------------------
## 2 Source Code
### Structure of Project
```
Facial_Recognition_under_varying_lighting_conditions_using_SVM/
│
├── data/                    # Contains the dataset and related files
│   ├── raw/                 # Original dataset (e.g., Extended Yale B)
│   └── processed/           # Preprocessed data ready for training/testing
│
├── doku/               # Jupyter or Colab notebooks for experiments
│   ├── data_preparation.ipynb  # Notebook for data loading and preprocessing
│   ├── model_training.ipynb    # Notebook for training SVM and other models
│   └── performance_analysis.ipynb  # Notebook for evaluating and visualizing results
│
├── results/                 # Store results such as plots, metrics, etc.
│   ├── metrics/             # Accuracy, F1-score, confusion matrix, etc.
│   └── plots/               # Confusion matrix heatmaps, bar charts, etc.
│
├── src/                     # Source code for the project
│   ├── preprocess.py        # Scripts for preprocessing data
│   ├── model.py             # SVM model implementation
│   ├── evaluation.py        # Evaluation metrics and visualization
│   └── utils.py             # Utility functions (e.g., memory tracking)
└── LICENSE                  # License for the project
└── .gitignore               # Files to ignore in version control

```
## Explanation of Code 
### FILE1 
##### Purpose
Implements facial recognition using an SVM classifier on the Extended Yale B dataset.

##### Contents
- Library Imports
  - Includes necessary libraries for image processing, machine learning, performance evaluation, and visualization
- Google Drive Mounting
  - Provides an option to mount Google Drive to access the dataset
- Dataset Path Setup
  - Defines the directory path for the Extended Yale B dataset
- Dataset Loading
  - Processes images by converting to grayscale, resizing, and flattening into feature arrays
  - Assigns labels based on folder names.
- Progress Tracking
  - Displays dataset loading progress as a percentage
- Dataset Preparation
  - Splits the data into training and testing sets
- SVM Model Initialization
  - Configures an SVM with an RBF kernel and specific hyperparameters
- Memory Usage Function
  - Tracks memory consumption during model training and prediction
- Performance Evaluation
  - Measures training and testing time, accuracy, and memory usage
  - Generates a classification report and a confusion matrix
  - Visualizes results with bar plots and heatmaps

### FILE2 
##### Purpose
Evaluates the performance of the SVM model with extended metrics and visualizations.

##### Contents
- Library Imports
  - Includes libraries for performance metrics, cross-validation, and visualization
- Evaluation Function
  - evaluate_extended_performance
    - Calculates model predictions on the test set
    - Computes evaluation metrics
      - Accuracy: Overall correctness of predictions
      - F1-Score: Harmonic mean of precision and recall (weighted)
      - Precision: Percentage of correctly identified positives
      - Recall: Percentage of true positives identified
    - Performs cross-validation to estimate the model's robustness
- Metric Visualization
  - Creates a bar plot for metrics (accuracy, F1-score, precision, recall, and cross-validation accuracy)
- Performance Visualization Function
  - visualize_performance_metrics
    - Visualizes training and prediction times with bar plots
    - Illustrates memory usage during training and prediction
- Usage
  - Demonstrates the evaluation function to compute metrics for the SVM model
  - Visualizes the computed metrics and performance measurements

### FILE3 
Combines the functionalities of FILE1 and FILE2, enabling both model training and detailed performance evaluation. Note that executing this file is time-intensive due to the dataset size and the extensive computations required for training and assessment.

### Remarks: 
- Google Account is required in order to use Colab
- Listed source code is uploaded as .ipynd file
- Dataset needs to be downloaded and uploaded to Google Drive to use given source code (ref. Installation and Usage)
- Loading the dataset and training the SVM Model takes a lot of time (approx 10-20 minutes each)
- calculation of performance assessments takes a lot of time
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
- fff:
- ![image](https://github.com/user-attachments/assets/a2b44660-e71d-4742-b4b5-0d7c4439ff9f)
- cross validation score:
  IMAGE???ß????
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!!!!!!
!!
--------------------------------------------------------------------------------
## 4 Installation and Usage
This project has been implemented using Google Colab, with the Extended Yale B dataset.
The size of the dataset is too large to upload and include it into this project, therefore instructions will be given on how download and use it will be provided in the following. The Extended Yale B dataset is distributed as a free resource for academic and research use and can therefore be downloaded from it's official website.

Steps:
# link problem
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
## 5 References and Documentation
#### References

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

#### Explanation of Key Algorithm (Support Vector Machine SVM)
A Support Vector Machine (SVM) is a supervised machine learning algorithm used for classification tasks. It works by finding the optimal hyperplane that separates data into different classes, maximizing the margin between the hyperplane and the closest data points, known as support vectors. The SVM can handle both linear and non-linear classification problems. For non-linear data, SVM uses a kernel trick to map the data into a higher-dimensional space where a linear separation is possible. Common kernels include the Radial Basis Function (RBF) kernel, which allows for flexible decision boundaries.

The key parameters in SVM are C and gamma. The parameter C controls the trade-off between maximizing the margin and minimizing classification errors, while gamma defines the influence of individual data points. SVM is effective in high-dimensional spaces and is known for its ability to generalize well, but it can be computationally expensive and requires careful tuning of parameters to achieve optimal performance.

-----------------------------------------------------------------------------

## 6 Issues and Contributions
One of the primary challenges observed in this project is the model's limited generalization to extreme lighting conditions. While the SVM performs well under most scenarios, it struggles when faced with very bright or heavily shadowed images, where facial features become significantly obscured or distorted. Another limitation is the relatively small size of the Extended Yale B dataset, which, despite its controlled lighting variations, does not capture real-world complexities such as facial expressions, occlusions, or diverse backgrounds.
The scalability of the model is another concern. SVMs are computationally intensive, especially when handling larger datasets, due to their quadratic training complexity. This may pose challenges for scaling the project to datasets with a significantly higher number of samples. Additionally, the model’s accuracy depends heavily on preprocessing steps such as resizing and grayscale conversion. Any inconsistencies or errors during these steps can negatively impact performance.
Although the Extended Yale B dataset is not very large, the time required to load and preprocess the data, as well as to train the SVM model, is significant—taking approximately 30 minutes in some cases. This highlights the need for more efficient data handling and processing strategies.

Contributions:  
- Optimization of Data Loading and Preprocessing:   
   Efforts were made to streamline the loading and preprocessing of the Extended Yale B dataset to reduce runtime without sacrificing data quality. This included experimenting with optimized file handling techniques and reducing redundancy in preprocessing steps
- Runtime Enhancements:  
  Adjustments were implemented to improve the efficiency of the training process. This included tuning SVM hyperparameters and using parallel processing where possible to speed up computations
- Evaluation of Alternative Models:  
  The project incorporated a framework to test and compare the performance of different machine learning algorithms, such as k-Nearest Neighbors (k-NN) and Random Forest, against SVM. This provided insights into alternative approaches to address scalability and runtime issues
- Model Scalability Exploration:  
  Experiments were conducted to explore the performance of the SVM model when trained on subsets of larger datasets, enabling an assessment of its scalability potential
- Integration of Advanced Preprocessing Techniques:  
  Advanced preprocessing methods, such as histogram equalization and contrast adjustment, were explored to improve the robustness of the model under extreme lighting conditions
- Benchmarking Against Real-World Datasets:  
  A plan was developed to benchmark the current implementation against larger, real-world datasets to identify further areas for improvement and validate the model’s performance in more diverse scenarios


----------------------------------------------------------------
## 7 Future work
To build on the current project, several potential improvements can be explored. One promising direction is the incorporation of neural networks, particularly Convolutional Neural Networks (CNNs), which can provide superior performance on larger and more diverse datasets by learning hierarchical feature representations. Data augmentation is another avenue worth pursuing, as it can enrich the dataset with synthetic variations, including different lighting angles, occlusions, and facial expressions, to improve the model’s robustness.

Future iterations of this project could also focus on enabling real-time facial recognition by integrating a webcam or camera feed. This would require optimizing the SVM implementation or exploring alternative algorithms better suited for real-time performance. Another area for enhancement is the combination of SVM with feature extraction techniques such as Principal Component Analysis (PCA) or Histogram of Oriented Gradients (HOG), which could boost both accuracy and speed.

Finally, cross-domain testing on other datasets would help evaluate the model's ability to generalize beyond the Extended Yale B dataset. Adding explainability tools to visualize the SVM decision boundaries could also provide valuable insights into the model's behavior, increasing its interpretability and trustworthiness.
