# ECG Heartbeat Categorization

## Introduction

This notebook documents how we trained a convolutional neural network (CNN) model from a given set of electrocardiogram (ECG) heartbeat data to classify different heartbeat classes. It includes EDA, models training and testing.

## About Dataset

**Introduction**

This dataset is composed of two collections of heartbeat signals derived from two famous datasets in heartbeat classification, the [MIT-BIH Arrhythmia Dataset](https://www.physionet.org/content/mitdb/1.0.0/) and the [PTB Diagnostic ECG Database](https://www.physionet.org/content/ptbdb/1.0.0/). The number of samples in both collections is large enough for training a deep neural network.

This dataset has been used in exploring heartbeat classification using deep neural network architectures, and observing some of the capabilities of transfer learning on it. The signals correspond to electrocardiogram (ECG) shapes of heartbeats for the normal case and the cases affected by different arrhythmias and myocardial infarction. These signals are preprocessed and segmented, with each segment corresponding to a heartbeat.

**Content:**

<font color =orange>**The MIT-BIH Arrhythmia Dataset**</font>
- Number of Samples: 109446
   
- Number of Categories: 5

- Sampling Frequency: 125Hz

- Data Source: Physionet's MIT-BIH Arrhythmia Dataset

- Classes: ['N': 0, 'S': 1, 'V': 2, 'F': 3, 'Q': 4]

  - N: Normal beat
  - S: Supraventricular premature beat
  - V: Premature ventricular contraction
  - F: Fusion of ventricular and normal beat
  - Q: Unclassifiable beat


<font color =orange>**The PTB Diagnostic ECG Database**</font>
- Number of Samples: 14552

- Number of Categories: 2

- Sampling Frequency: 125Hz

- Data Source: Physionet's PTB Diagnostic Database


<font color = red>**Remark:**</font> *All the samples are cropped, downsampled and padded with zeroes if necessary to the fixed dimension of 188.*

**Data Files**

This dataset consists of a series of CSV files. Each of these CSV files contain a matrix, with each row representing an example in that portion of the dataset. The final element of each row denotes the class to which that example belongs.

**Acknowledgements**

Mohammad Kachuee, Shayan Fazeli, and Majid Sarrafzadeh. "ECG Heartbeat Classification: A Deep Transferable Representation." [arXiv preprint arXiv:1805.00794 (2018).](https://arxiv.org/abs/1805.00794)

**Provider:** Shayan Fazeli

**Reference:** https://www.kaggle.com/datasets/shayanfazeli/heartbeat/data


## About this notebook

For this notebook, we refer the source code shared by Gregoire DC on Kaggle as a reference.
(https://www.kaggle.com/code/gregoiredc/arrhythmia-on-ecg-classification-using-cnn/notebook)
