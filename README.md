## Institute Technical Summer Project
A pen-type portable device and a trajectory recognition algorithm.

[Flowchart](/Images/Flowchart.jpeg)

**Signal acquisition**
The acceleration signals measured from the triaxial accelerometer are transmitted to a computer via the wireless module. Users can utilize this digital pen to write digits and make hand gestures at normal speed. The measured acceleration signals of these motions can be recognized by the trajectory recognition algorithm. 

 - Accelerometer: The acceleration signals of hand motions are measured by the pen-type portable device
 - Gyroscope: To improve accelerometer accuracy
 - Magnetometer: To recalibrate the sensor

**Signal Preprocessing**
The signal preprocessing procedure consists of: 

 - Calibration( to remove drift errors and offsets from the raw signals )
 - A moving average filter( to remove high frequency noise from raw data )
 - A high-pass filter( to remove gravitational acceleration from raw data )
 - Normalization

*The raw acceleration signals of hand motions are generated by the accelerometer and collected by the microcontroller. Due to human nature, our hand always trembles slightly while moving, which causes a certain amount of noise.*

**Feature Generation**
The characteristics of different hand movement signals can be obtained by extracting features from the pre-processed x, y, and z-axis signals

**Feature Selection**
Because the amount of the extracted features is large, we adopt Kernal-Based Class Separability to select most useful features and then use Linear Discriminant Analysis to reduce the dimensions of features.

Before classifying the hand motion trajectories, we perform the procedures of feature selection and extraction methods. In general, feature selection aims at selecting a subset of size m from an original set of d features (d > m) 

Therefore, the criterion of kernel-based class reparability (KBCS) with best individual N (BIN) is to select significant features from the original features (i.e., to pick up some important features from d). 

**Feature Extraction**
Linear discriminant analysis (LDA) is to reduce the dimension of the feature space with a better recognition performance (i.e., to reduce the size of m). The objective of the feature selection and feature extraction methods is not only to ease the burden of computational load but also to increase the accuracy of classification.

**Classifier**
The reduced features are used as the inputs of classifiers. In this project, we are going to adopt a probabilistic neural network (PNN) as the classifier for handwritten digit and hand gesture recognition.

[Block Diagram](/Images/Block%20diagram.jpeg)

#### Links to Documentation

 - [Final Documentation](https://docs.google.com/document/d/1eJqBa40CPGVSAjVPga0h5ZBtP_GfkC4jkALfkZNsrUk/edit)
 - [Two Page Documentation](https://docs.google.com/document/d/1VDUPizK79FmGiAJCUSacQf7sq-F9xhPe6UNA24ouiEk/edit)
 - [Final Presentation](https://docs.google.com/presentation/d/13ECMv_6HX_5BkdorZ3mrw2cdAeByihjqaWwI72OVzTo/edit#slide=id.p)
