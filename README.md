# CS7641: Project Proposal
## Introduction
ML in agriculture uses image analysis to detect diseases early, boosting crop health and yields. It works by training models on data (images of healthy & diseased plants) to identify disease patterns. Existing literature includes Ramcharan et al. which explores the use of deep learning for detecting disease in Cassava (major staple in Africa) [1]. They used transfer learning to construct a deep CNN to identify a few different diseases on this crop to somewhat accurate results. In a paper by Ferentinos, they use CNNs to identify diseases on the leaves of plants [2]. In a paper by Mohanty et al. they looked at 26 diseases across 14 plant species and achieved a model in training with an accuracy of 99.35% [3]. Our dataset (Five Crop Diseases Dataset) contains images of five different crops, with each crop containing healthy and diseased images. For example, diseases for corn include common rust, gray leaf spot, and northern leaf blight. Overall, there are 17 classes (crop x disease combination) and over 13,000 images.

## Problem Statement
The problem we're tackling involves quickly and accurately identifying diseases in a specific crop, i.e. corn, using machine learning. This is crucial because diseases can drastically reduce crop yields and quality, leading to significant economic losses. Our motivation is to develop a tool that simplifies disease detection for farmers, helping them make better treatment decisions and ultimately improving crop health and productivity.

## Methods
Some image preprocessing techniques we decided on are cv2.resize, to ensure image dimensions uniformity; cv2.sift_create, to extract feature descriptors from images; and grayscale conversion (cv2.cvtColor), to eliminate color channels for the models to focus on structure as opposed to color.

We thought of two supervised models: Convolutional Neural Networks—which can recognize intricate patterns and features in images through convolution layers, and Support Vector Machines—which can find accurate hyperplanes that separate the high-dimensional feature space built using SIFT feature descriptors.

Unsupervised model: K-means Clustering - divides image sets into clusters based on vector similarity instead of labels. This can be extremely useful for classification after assigning labels to the clusters.

## Metrics 
Some quantitative metrics for the Convolutional Neural Network would be accuracy (% of correctly classified images), precision (proportion of true positives), recall (proportion of true positives among true positives), F1 score (harmonic mean of precision and recall), and the loss function (cross-entropy loss in training). 

Similarly, for the SVM, accuracy, precision, recall, F1 score, and Area Under the ROC Curve (quantified ability to distinguish between classes) would be good metrics to track. 

For K-Means Clustering, the silhouette coefficient (similarity within clusters compared to between clusters) and the Calinski-Harabasz index (separation between clusters) will be used as metrics.


### Goals
- Achieve high accuracy (>90%) in classifying.
- Maintain a balanced precision and recall with F1-score (>85%).
- Minimize the loss function value.
- Achieve a high AUC (>0.9) for class separation.
- Achieve a high silhouette coefficient (>0.5).
- Maintain high Calinski-Harabasz and Davies-Bouldin indices (>1).

### Expected Results
The CNN should accurately distinguish between healthy and diseased crops, with minimal misclassifications.


## Gantt Chart
[(link to gantt chart)](https://gtvault-my.sharepoint.com/:x:/g/personal/jpurkar3_gatech_edu/EZ0NvVTVG0xOvP2TG49LMQ0Blx8_oc7quM3DplCroAo2sw)

## Contribution Table
| Member        | Task                                                  |
| ------------- | ----------------------------------------------------- |
| Brandon       | Github page update and repo descriptions              |
| Ojasw         | Model coding and training                             |
| Janhavi       | Problem Statement, background, Gantt Chart            |
| Samarth       | Data preprocessing                                    |
| Aditya        | Quantitative metrics,results evaluation and analysis  |

## References
[1] Ramcharan, A., Baranowski, K., McCloskey, P., Ahmed, B., Legg, J., & Hughes, D. P. (2017). Deep Learning for Image-Based Cassava Disease Detection. Frontiers in plant science, 8, 1852. https://doi.org/10.3389/fpls.2017.01852

[2] Ferentinos, K. P. (2018). Deep learning models for plant disease detection and diagnosis. Computers and Electronics in Agriculture, 145, 311-318. https://doi.org/10.1016/j.compag.2018.01.009

[3] Mohanty, S. P., Hughes, D. P., & Salathé, M. (2016). Using Deep Learning for Image-Based Plant Disease Detection. Frontiers in plant science, 7, 1419. https://doi.org/10.3389/fpls.2016.01419
