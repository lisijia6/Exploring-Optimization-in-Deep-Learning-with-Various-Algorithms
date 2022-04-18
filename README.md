# Exploring-Optimization-in-Deep-Learning-with-Various-Algorithms

**This is the final project for MIE424 (Optimization in Machine Learning).**


**Project Team: ** Jiahua Chen, Keying Chen, Jiaru Li, and Sijia Li


**Abstract** — The world has been fighting against COVID-19 for more than two years. Given the urgency of early and accurate detection of COVID-19 cases, deep learning is a promising technique for identifying COVID-19 cases and preventing the infection from spreading. This project aims to use the DenseNet121 architecture, a dense convolutional neural network, to diagnose COVID-19 patients from chest X-ray images. The project will compare the performances of various optimization algorithms, such as SGD, Adam, and their variants. Through tuning different sets of hyperparameters for each optimizer, applying early stopping based on validation error during training, and using Binary Cross Entropy as the loss function, the best non-adaptive and adaptive optimization algorithms are selected according to validation and test errors. They are SGD with Nesterov momentum and Adamax. A trade-off between convergence speed and classification error for the two best performing optimizers is observed. Compared to Adamax, SGD with Nesterov momentum has superior performance in terms of validation and test accuracies, but has a slower convergence speed. Moreover, our results show that SGD with Nesterov momentum has the highest test accuracy of 94%, arriving at a different conclusion compared to other papers performing similar optimizer evaluations on COVID-19 chest X-ray images.


**In this repository:**
1. The **Data** folder contains the original as well as pre-processed COVID-19 chest X-ray images used in this project.
2. The **Notebooks** folder contains the code for this project. 
    * **MIE424_Project_Data_Processing.ipynb** is the code for pre-processing the data, including converting image files to tensors and performing data augmentation. 
    * **Model_Architecture.ipynb** is the code for building the model (feature extraction using pretrained DenseNet121, COVID-19 prediction using new classifier), importing various optimizers implemented by [**Nicklas Hansen**](https://github.com/nicklashansen/neural-net-optimization), and defining model training and evaluation functions.
    * **Model_Architecture_sgd_lrd.ipynb, Model_Architecture_SGD_w_momentum.ipynb, Model_Architecture_Adam_AdamLRD.ipynb, Model_Architecture_AdamL2.ipynb, and Model_Architecture_AdamW.ipynb** are the notebooks for training our model using various optimization algorithms (SGD, SGD with momentum, SGD with Nesterov momentum, SGD with Learning Rate Dropout, Adam, Adam with Learning Rate Dropout, AdamL2, AdamW, and Adamax) with a wide range of hyperparameter combinations (e.g., varying batch size, varying learning rate). 
