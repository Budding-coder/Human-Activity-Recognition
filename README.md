# Human-Activity-Recognition

## Description:

These days Smartphones have become an integral part of our life where we cannot assume our life without a mobile phone. Smartphones have very
interesting sensors in addition to cameras. These sensors are very useful when playing games and enhances the user experience.
Two such sensors are called Accelerometer and Gyroscope. Accelerometer measures acceleration and Gyroscope measures angular velocity.
 
Here we are tying to collect the data from Accelerometer and Gyroscope and use this data to predict the activity that the person is 
performing. 


## Problem Statement :

Problem statement is, we are trying to determine what is the activity that the human is performing using sensors that we have in smart
phones. 
This project is to build a model that predicts the human activities such as Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing or Laying.
We are building a 6-class classifier.

## Why is this useful :

These daya many people are using smart watches like Fitbit or Apple watch etc., to track sleep and activity levels of the day. These
watches internally contains an Accelerometer and Gyroscope. These records the human activity data and we use this data to determine
if we are actually running , walking , Walking_Upstairs, Walking_Downstairs etc,. Using all this data, Accelerometer and Gyroscope predicts how many calories are burnt or hours of sleep , heartbeats using heart-rate sensors. 

So by using these sensors, we are trying to predict human activities. We can use these activities and map them to one of the measures , 
like how many calories are burnt, how many hours of sleep etc .
Hence, a person who has Smartphone can monitor his/her health using these sensors and predictions. This experiment was video recorded to label the data manually.

Accelerometers are Tri-axial, which means, they measure accelaration on X-axis, Y-axis and Z-axis measured over time. Gyroscopes are also Tri-axial, which means, they measure velocity on X-axis, Y-axis and Z-axis and also there is time series for X,Y,Z axis. 

In most smartphones there are triaxial sensors. 

## Business Problem 

This project is to build a model that predicts the human activities such as Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing or Laying. We are building a 6-class classifier.

This dataset is collected from 30 persons(referred as subjects in this dataset), performing different activities with a smartphone to their waists. The data is recorded with the help of sensors (accelerometer and Gyroscope) in that smartphone.

As input there is 6 time series data for both Accelerometers and Gyroscopes for each axis. Using this input, we predict one of the 6 human activities mentioned above.

This is a multi-class classification problem. The metric we use is accuracy, confusion matrix (to see for which class model is performing well and for which class is it not), multi class log-loss. 

## How data was recorded

By using the sensors(Gyroscope and accelerometer) in a smartphone, they have captured '3-axial linear acceleration'(_tAcc-XYZ_) from accelerometer and '3-axial angular velocity' (_tGyro-XYZ_) from Gyroscope with several variations. 

> prefix 't' in those metrics denotes time.

> suffix 'XYZ' represents 3-axial signals in X , Y, and Z directions.

## Feature names

1. These sensor signals are preprocessed by applying noise filters and then sampled in fixed-width windows(sliding windows) of 2.56 seconds each with 50% overlap. ie., each window has 128 readings. 
We take each window of data and apply some filters like signal processing type, on the window data  and then converted into a fixed length vector.
2. From Each window, a feature vector was obtianed by calculating variables from the time and frequency domain.
> In our dataset, each datapoint represents a window with different readings 

Next window of data is taken like, 50% of part from first window which is overlapping and 50% of part in second window.  Then filter and sampling is applied on this data and is converted into numerical vector of fixed size.

This process is continued to all 6 time series data . Each vector is of size 128.
3. The accelertion signal was saperated into Body and Gravity acceleration signals(___tBodyAcc-XYZ___ and ___tGravityAcc-XYZ___) using some low pass filter with corner frequecy of 0.3Hz.

4. After that, the body linear acceleration and angular velocity were derived in time to obtian _jerk signals_ (___tBodyAccJerk-XYZ___ and ___tBodyGyroJerk-XYZ___). 

5. The magnitude of these 3-dimensional signals were calculated using the Euclidian norm. This magnitudes are represented as features with names like _tBodyAccMag_, _tGravityAccMag_, _tBodyAccJerkMag_, _tBodyGyroMag_ and _tBodyGyroJerkMag_.

6. Finally, We've got frequency domain signals from some of the available signals by applying a FFT (Fast Fourier Transform). These signals obtained were labeled with ___prefix 'f'___ just like original signals with ___prefix 't'___. These signals are labeled as ___fBodyAcc-XYZ___, ___fBodyGyroMag___ etc.,.

## Constraints:

1. Some form of interpretability.
2. There is no low latency requirement here.

## Libraries used

1. ipython-notebook - Python Text Editor
2. sklearn - Machine learning library
3. seaborn, matplotlib.pyplot, - Visualization libraries
4. numpy, scipy- number python library
5. pandas - data handling library
6. keras - Used for making deep learning models
7. hyperas - used for tuning hyper-parameters for deep learning models


