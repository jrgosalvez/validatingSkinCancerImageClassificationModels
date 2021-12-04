# Skin Cancer Image Classification: Malignant or Benign
SJSU DATA 245 - ML Tech. Applying various classification models learned as a precursor to GAN and alternative semi-supervised machine learning methods.
#### Jie Dong, Rick Gosalvez, Canaan Law, Chitra Priyaa Sathya Moorthy, Haotong Qiu, and Lianglei Zhang. 
#### Team 2 Project, DATA 245, Fall 2021
Various methods for supervised classification of images exist, each with its own pros and cons. Our team leveraged a clean Kaggle image dataset to study four supervised image classification methods and one supervised type of deep learning to assess model performance and explore which offered the most flexibility/reliability for future work. In this blog, we will share our process, findings, and main takeaways.
### Motivation
Image classification is an increasingly popular function. In the field of medicine benefits include enabling machine supported diagnosis for patients that historically might not have access to proper health care. In this vein, our team chose a publicly available skin cancer dataset to preprocess, develop models for, tune, and compare.
### Problem
Labeling data is expensive. As datasets expand, leveraging a model general enough to accommodate variations in image sets as they scale is an important challenge our team set out to explore. Our goal was to assess how the development and comparison of various supervised classification models to a supervised type of deep learning model could provide insights which could ultimately lead to semi-supervised learning approaches for scaling datasets.
### Solution
Support Vector Machine (SVM), K Nearest Neighbor (KNN), Decision Tree, Random Forest supervised learning models were created and compared to a Convolution Neural Network (CNN) deep learning model to identify which model most reliably and accurately predicted classifications to expand learning on a growing image dataset.
### Method
Our team deployed a simplified approach to validate image classification models:
1. Clean Kaggle Skin Cancer Image dataset to simplify evaluation.
2. Jupyter notebooks for coding and visuals: explore, preprocess, model, visualize, tune, compare, and save.
3. Github for collaboration and code management.

Data preprocessing techniques included image cleaning (cropping and blur) and converting data to numeric RGB color values normalized by a value of 255 to a range of 0–1, making it possible to classify images based on numeric values within the dataset. Image regularization was essential for a more uniform analysis of the dataset. String labels were converted to binary labels (malignant and benign). Train and test datasets were merged after labeling and shuffled to reduce bias and facilitate additional analysis and model validation.

Models resolved in 10 to 15 minutes for the initial dataset, requiring additional computational time for expanded datasets on personal devices. Models were saved as Pickle files for future use where weighting could be saved for improved processing speed.
### Outcome
Preprocessing data supported all models to attain 75% accuracy or better on the dataset. This makes sense because the dataset was clean. Benefits bifurcated models as the dataset was expanded.
CNN outperformed other model alternatives on the dataset and on an expanded dataset affording a model accuracy of 85.8% without overfitting. CNN requires larger datasets for training making it a strong model for expanding datasets.
### Takeaways
<li> Start small. Tune. Save models. Then apply to larger datasets.
<li> Preprocessing significantly enhances performance of models.
<li> Data augmentations cropping and blur yield reliable results.
<li> ‘Lazy learning’ (e.g. KNN) and ‘ensemble’ (e.g. Random Forest) methods can yield computational challenges for scaling datasets.
<li> Neural Networks offer greater flexibility to other supervised learning methods for larger datasets.

### Future Work
Findings are promising, but not groundbreaking. To expand upon work, our team suggests continuing to grow the dataset with non-labeled images and incorporating k-fold cross validation. Applications and images should be centralized on a cloud platform linked to a mobile application to facilitate dataset expansion and scheduled model recalculations to avoid model drift while enabling automation.

Further, we believe that extending to a Generative Adversarial Network (GAN) solution and comparing to alternatives modeled for this project would be an interesting exercise.
