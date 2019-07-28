 
# AUTOMATIC- FACE- RECOGNITION

## What is Facial Recognition?
 
- Facial Recognition is a biometric software application which can identify a person through his or her digital image. When facial-recognition is to be used as part of a biometrics-based security system, individuals allow several digital images or pictures of themselves to be taken, with different facial expressions and at different angles. For verification, the individuals stand in front of the camera for a few seconds, and the resulting image is compared using facial-recognition software to the digital images that have been previously saved on a given database.

## FEW APPLICATIONS:
- __Facial Recognition and Access Control in buildings__
Making sure that buildings are safe from unauthorized entry is essential. You need to install proper security measures to control who enters and exits your building. Biometric Facial Recognition is an advanced and effective tool which offers excellent control and security at your building.

- __Facial-Recognition and security for banks__
With increasing security challenges, banks and financial institutions are now incorporating biometric security technology into their platforms. The biometric security system is currently to replacing personal identification numbers (PINs) and password protection methods which are easily counterfeited. Facial Recognition is the preferred choice in the financial sector because it can be used to:
1. __Face-login:__ customer can access their accounts using face identification. This will also reveal an impostor trying to access your account.
2. __Fraud prevention:__ The system’s algorithm allows you to logically analyze and collect information from image databases and help recognize fraudsters just steps away from the bank.

## Steps:

- __This consists of 3 steps:__

1. Collecting Data and preprocessing
2. Extraction of Features from Images
3. Classifcation

## Objective:

Building a deep learning model that can recognize the person by recognizing their face.
So, in the first step we can collect the images of people residing in a colony,bank,office etc. ,build our dataset , and after that extract features from images using CNN and then apply Classification Models.

## ML Model and Transfer Learning:

## - APPROACH 1:

-	__Extraction of Feature:__
We can use VGG-16(16-layers Convolutional Neural Network) CNN model in order to extract features from the images. This method is also known as transfer learning.
 
- __Training of XgBoost-Model on the Features:__
Using this we can extract features from images , which can be used by XgBoost to classify the people in the database.
 
## But why use XgBoost? Why not Softmax or SVM ?

- Classifiers on top of deep convolutional neural networks
As mentioned before, models for image classification that result from a transfer learning approach based on pre-trained convolutional neural networks are usually composed of two parts:

1. __Convolutional base__, which performs feature extraction.
2. __Classifier__, which classifies the input image based on the features extracted by the convolutional base.
- Different approaches can be followed to build the classifier:

1. __Fully Connected Layers:__ For image classification problems, the standard approach is to use a stack of fully-connected layers followed by a softmax activated layer . The softmax layer outputs the probability distribution over each possible class label and then we just need to classify the image according to the most probable class. SOFTMAX Classifier is MultiClass Classification + Logistic Regression.
2. __Linear support vector machines:__ Linear support vector machines (SVM) is another possible approach.But in linear models like SVM choosing the right kernel can be difficult.
3. __XgBoost:__ XGBoost is an ensemble method as it uses many trees to take a decision so it gains power by repeating itself. Also, Tree based approaches are very robust.

## - APPROACH 2:
- __Haar-like features__ are digital image features used in object recognition. They owe their name to their intuitive similarity with Haar wavelets and were used in the first real-time face detector.
- A Haar-Feature is just like a kernel in CNN, except that in a CNN, the values of the kernel are determined by training, while a Haar-Feature is manually determined.
- Haar Cascades use the Ada-boost learning algorithm which selects a small number of important features from a large set to give an efficient result of classifiers then use cascading techniques to detect face in a image.
- Here are some Haar-Features. The first two are “edge features”, used to detect edges. The third is a “line feature”, while the fourth is a “four rectangle feature”, most likely used to detected a slanted line.
 

## The LPBH Face Recognizer :
- There are different types of face recognition algorithms, for example:
· __Eigenfaces (1991)__
· __Local Binary Patterns Histograms (LBPH) (1996)__
· __Fisherfaces (1997)__
· __Scale Invariant Feature Transform (SIFT) (1999)__
· __Speed Up Robust Features (SURF) (2006)__

## EXPLANATION:
- __Local Binary Pattern (LBP)__ is a simple yet very efficient texture operator which labels the pixels of an image by thresholding the neighborhood of each pixel and considers the result as a binary number.
 
## Testing / Detecting :

- After detecting the face , based on confidence levels, we can say whether the person is really the one or not.
 .
## REFERENCES:
1. https://medium.com/@krsatyam1996/haar-cascade-face-identification-aa4b8bc79478
2. https://towardsdatascience.com/face-recognition-how-lbph-works-90ec258c3d6b
3. https://sightcorp.com/blog/how-biometric-facial-recognition-is-improving-security/

