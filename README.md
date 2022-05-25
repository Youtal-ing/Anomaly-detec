# Anomaly-detection

 Detecting anomalies has been a research topic for a long time. Due to the increasing amount of data collected in the modern world in broad domains such as risk management, compliance, security, financial surveillance, health and medical risk, and AI safety, the need for automated data analysis has become a necessity. One of the most critical tasks in data analysis is the detection of anomalous data points.in this project we will use **LSTM** 
 
# What is LSTM ? : 
Long short-term memory  usually just called “LSTMs” – are a special kind of RNN, capable of learning long-term dependencies. They were introduced by Hochreiter & Schmidhuber (1997) ,it's an artificial neural network used in the fields of artificial intelligence and deep learning. Unlike standard feedforward neural networks, LSTM has feedback connections. Such a recurrent neural network can process not only single data points (such as images), but also entire sequences of data.
A common LSTM unit is composed of a cell, an input gate, an output gate and a forget gate.The cell remembers values over arbitrary time intervals and the three gates regulate the flow of information into and out of the cell.LSTM networks are well-suited to classifying, processing and making predictions based on time series data

![](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-chain.png)
# For the comparison we will use the PyOD Library for anomaly detection and we will generate random data

# Dataset :
The dataset is open source, From Kaggle (is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment).
The data set represents 219,521 readings from 51 sensors  that are used to do condition monitoring of pumps.**Our purpose is to detect these abnormal observations in advance**
**Dataset details :** 

-  Timestamp data
-  Sensor data(52 series): All values are raw values
-  Machine status: This is target label that we want to predict when the failure will happen


**to download the data :** 
// !kaggle datasets download -d nphantawee/pump-sensor-data

**Tools and libraries used :**

-   Python
    -   Pandas
    -   seaborn
    -   numpy
    -   matplotlib
    -   Sklearn(PCA)
    -   VAR
    -   Tensorflow
    -   keras
    -   PyOD
