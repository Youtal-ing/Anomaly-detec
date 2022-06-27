# Anomaly-detection

 Detecting anomalies has been a research topic for a long time. Due to the increasing amount of data collected in the modern world in broad domains such as risk management, compliance, security, financial surveillance, health and medical risk, and AI safety, the need for automated data analysis has become a necessity. One of the most critical tasks in data analysis is the detection of anomalous data points.

# For the Benchmark we will use the PyOD Library for anomaly detection and we will generate random data

# For the time series use case we will use vector autoregressive (VAR) model // and  Vae Model (in both cases we will aplly PCA first)  
 
# What is VAR Model?
Vector autoregression (VAR) is a statistical model used to capture the relationship between multiple quantities as they change over time. VAR is a type of stochastic process model. generalize the single-variable (univariate) autoregressive model by allowing for multivariate time series. VAR models are often used in economics and the natural sciences.

# what is Vae Model :

# specifically we will use Sequence to Sequence Model (Encoder-Decoder Long Short-Term Memory Networks) :

**The Encoder-Decoder LSTM can be implemented directly in the Keras deep learning library.

![](https://miro.medium.com/max/1400/1*bY_ShNK6lBCQ3D9LYIfwJg@2x.png)

The general idea of autoencoders is pretty simple and consists in setting an encoder and a decoder as neural networks and to learn the best encoding-decoding scheme using an iterative optimisation process. So, at each iteration we feed the autoencoder architecture (the encoder followed by the decoder) with some data, we compare the encoded-decoded output with the initial data and backpropagate the error through the architecture to update the weights of the networks.

In VAE, the encoder also learns a function that takes a vector of size n as input.However, instead of learning how to generate potential vectors that the decoder function can reproduce, as in traditional AEs, VAE generates two vectors (size m) that represent the parameters of the distribution (mean and variance). Learn to do. The latent vector is sampled and the decoder function can convert it back to the original input vector[


# Before we will apply PCA : 
**Principal component analysis (PCA) is a technique that transforms high-dimensions data into lower-dimensions while retaining as much information as possible.

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
  
 **Project Steps :** 

-  Loading Dataset
-  Cleaning Dataset
-  Analyzing Dataset
-  Applying PCA (The principal components)
-  Building (Decoder , Encoder)
-  Training 
-  Model Loss /  precision  /  recall / f1-score  / support
