# COVID-19-detection
Covid -19 detection using the X-ray images for the rapid action in health management sector


1. Introduction
COVID-19 is a life-threatening infectious disease caused by a newly discovered virus called noval corona virus (2019-nCOV). The disease erupted in late 2019 and spreads across countries across all continents affecting many people and has taken more lives. Due to high spread of disease, traditional diagnosing the disease like inspection of physical symptoms, clinical evidence consumes time.
Facts and Statistics
X-Ray review is one of the preliminary diagnostic methods to identify a patient is infected with Covid-19. Manual review may cause variation in interpreting the results and will lead multiple rounds of test, at time patient may not have time to take those diagnosis. So, a precise, simple and automated solution warranted to tackle the current situation to support the preliminary screening for Covid-19.
It is time that it is required the urgent establishment of precise and fast diagnostic tests to verify suspected cases, screen patients, and conduct virus surveillance. This establishment of precise, fast and inexpensive diagnostic tests methods can lower the risk of spreading infection, alleviate the strain on the healthcare system, and mitigate the cost of care for both individuals and the government and improve the health care system in addressing the disease. In this study, a focus on using medical images to diagnose Covid 19 will be established where by an algorithm will trained to analyze the images and classify patients to either have Covid 19 or not.
2. Project Objective:
The Objective of this course work is to create a machine learning algorithm to automatically detect the Covid-19 infection using digital chest X-Ray.
3. Role of Machine Learning:
Machine learning plays an important role in detection of Corona virus because other methods are slow lead to the severe spread of the pandemic causing more death.
Following are the methodology / steps planned
1. Apply pre-trained Convolutional Neural Network to classify Normal and Covid-19 X-Ray
2. Use the collected X-rays to train the model and apply the transfer learning process to classify the type of chest X-rays.
3. Classification Accuracy will be used as key performance metrics to gauge the performance of CNN model.
If model comes with high accuracy will help to perform the preliminary screening for potential Covid-19 patients by the radiologist
4. Data Exploration Large number of X-ray images are publicly available for machine learning and data research purpose in Kaggle. Kaggle with enormous volume of more than 50,000 public dataset across various areas for machine learning analysis has helped to have dataset for this study. The dataset has four categories of the images of the chest X-rays namely
● Covid-X-rays of COVID positive cases patients
● Viral Pneumonia- X-rays of patients shown pneumonia but not COVID
● ‘normal’- They have neither presented the symptoms of COVID nor pneumonia
● Pulmonary opacification
All the images are in Portable Network Graphics (PNG) file format and resolution are 299*299 pixels
Source: https://www.kaggle.com/tawsifurrahman/covid19-radiography-database
5. Feature Engineering
In this case study we have chosen VGG16. This model has won first prize in ILSVR competition in 2014. It is considered to be one of the excellent model architectures till date. It is a sequential model, so all the layers are arranged in a sequential order. From Keras ImageDataGenerator function is imported, since it has many image manipulation functions to rescale, rotate, zoom, flip etc. This function will not impact the data stored on the disk. The objective of ImageDataGenerator is to import data with labels easily into the model.![image](https://user-images.githubusercontent.com/48022963/113513136-b6809080-9585-11eb-97d0-f9e8f98f907e.png)
6. Building Training/Validation/Test Samples Team went ahead and created folders for training and test data set. ImageDataGenerator is used to Object both training and test data sets. The folder structure of the data as follows. IDG has the ability to label all the data inside the categorized folders, so data set will be readily prepped for neural network processing.![image](https://user-images.githubusercontent.com/48022963/113513191-00697680-9586-11eb-8378-69d1d0efc542.png)
![image](https://user-images.githubusercontent.com/48022963/113513195-052e2a80-9586-11eb-984e-1585ddf795ed.png)
![image](https://user-images.githubusercontent.com/48022963/113513197-09f2de80-9586-11eb-8907-b88a87e74289.png)

7. Model Selection Execution
After initialization, all the parameters and features are applied sequentially. After creating all the convolution, data passed to the dense layer. We have used 4 units of dense layer in the end with SoftMax activation as we have 2 classes to predict from at the end which are Covid-19 and Normal. The SoftMax layer will output the value between 0 and 1 based on the confidence of the model that which class the images belongs to.![image](https://user-images.githubusercontent.com/48022963/113513248-61914a00-9586-11eb-93a1-36de3749aee5.png)
8. Analysis and Preliminary Result
Model started has an incremental growth from 10th epoch till 47th epoch. From 40th epoch model has reached a state to yield 97% accuracy and from 47th epoch it is observed that there is loss in accuracy. Also validation accuracy is reached to 92% in 40th epoch![image](https://user-images.githubusercontent.com/48022963/113513278-943b4280-9586-11eb-87dc-d645ab0b9232.png)
![image](https://user-images.githubusercontent.com/48022963/113513281-98fff680-9586-11eb-81d9-ac2fc34de9b5.png)
9. Test Results and Summary
Model was run with 30 samples to validate the prediction with out labels. Results are summarized in the following table.![image](https://user-images.githubusercontent.com/48022963/113513298-a917d600-9586-11eb-820a-08cc0e75da1a.png)
![image](https://user-images.githubusercontent.com/48022963/113513301-acab5d00-9586-11eb-9c78-1ccba66516e3.png)
![image](https://user-images.githubusercontent.com/48022963/113513304-b208a780-9586-11eb-9af1-1f308d8a1c80.png)
![image](https://user-images.githubusercontent.com/48022963/113513307-b59c2e80-9586-11eb-88fc-bbf9fb1dcc8e.png)

