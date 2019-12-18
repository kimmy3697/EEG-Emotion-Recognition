# EEG Emotion Recognition
#### HSE Computer Science Student's Project
###### Authors: Soboleva Natalia & Glazkova Ekaterina

뇌파 신호의 정확한 분류는 비정상적 뇌활동 감지에 대한 의학 연구에 대한  솔루션을 를 제공할 수 있다고 하네요. 근데 early phases in order to threat it 은 뭔 소리지.... ㅅㅂ  
여튼 그래서 자기네들은 약간 다른 각도로 접근을 해볼건데 감정 분류를 할거랍니다. CNN이랑 RNN을 쪼인트 시켜서 디자인하고 AE 구조를 취해서 데이터의 High dimen
In this study we are looking at this task from slightly another angle -- emotions recognition. We design a joint of convolutional and recurrent neural networks with the usage of autoencoder to compress high dimentionality of the data.

Current project consists of EEG data processing and it's convolution using AutoEncoder + CNN + RNN

## Pre-processing
[Report on Data Preprocessing ](https://github.com/nasoboleva/EEG-Emotion-Recognition/wiki/Препроцессинг-данных)

Artifact &mdash; that is the term for all recorded activity that is not of cerebral origin. Artifacts can be divided into two groups: physiologic (arise from other parts of the brain, for example, body) and extraphysiologic (arise from, for example, technical equipment) artifacts.

To extract the most important features of EEG observations pre-processing is necessary. For data processing and visualization [MNE](https://mne-tools.github.io/stable/index.html#) &mdash; open-source Python software for human neurophysiological data including EEG was chosen. In this area there are two main state-of-art methods to process EEG signals:
Wavelet transform and independent component analysis (ICA).

## AutoEncoder
[Report on AutoEncoder](https://github.com/nasoboleva/EEG-Emotion-Recognition/wiki/AutoEncoder)

Autoencoder is a neural network which consists of two parts: encoder and decoder, both are neural networks. In the work we create contractive autoencoder. It means that the layer between encoder and decoder has less neurons than an input layer.

 In our task target representation is the same as input data - it proves that we do not lose any data. Moreover, autoencoder be used for data preprocessing - the aim representation might be data cleared from noise.

The first autoencoder consists of two fully-connected layers with ReLU activation function.

## Convolutional AutoEncoder
[Report on Convolutional AutoEncoder](https://github.com/nasoboleva/EEG-Emotion-Recognition/wiki/CNN-AutoEncoder)

 CNNs can find local dependencies and represent higher-level features as compositions of lower-level dependencies.
Another reason is that CNN is well-suited for the dimensional relevance representations. The main purpose for convolutional neural network is to exploit spatial connections between different features in each signal.

In current work we are planning on using three types of layers: convolutional layers, pooling layers and fully connected layers.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ5MDU5MTg1OSwxODAwNjUwMDUxXX0=
-->