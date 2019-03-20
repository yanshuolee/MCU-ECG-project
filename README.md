# MCU-ECG-project
## Abstract
We propose an approach based on one-dimensional convolutional neural network for classifying four categories of ECG－Normal, AF, Noise, and Others. In previous state-of-the-art researches, many of them used a spectrogram to train a neural network with a huge number of training parameters. In order to decrease the computational complexity and enhance efficiency, we developed a 1-D CNN with sequential data to make a classification. Besides, we developed an algorithm to deal with variable-length ECG recordings. We trained on two different data splits: 5-fold cross-validation and training-validation-test split. We first trained on 5-fold with grid search in order to find the optimal training parameters and evaluated F_1 score with average 5-fold. We then trained on 50:20:30 split and calculated accuracy and loss of our best model. As a result, our model obtained an F_1 score of 81.4 with 5-fold cross-validation. Our method of 1-D CNN outperformed one of the top scores using 2-D CNN from Physionet 2017 challenge.
## System architecture
![](system%20architecture.png)
## Comparison with 2D CNN architecture
| F1 score | AF |	Normal | Other | AVG |
| :---: | :---: | :---: | :---: | :---: |
| Proposed 1D CNN | 79.2 | 90.2 | 74.8 | 81.4 |
| [Electrocardiogram Classifcation CNN](http://www.cinc.org/archives/2017/pdf/070-060.pdf) | 79.0  | 87.8 | 70.1 | 78.9 |
| [Electrocardiogram Classification CRNN](http://www.cinc.org/archives/2017/pdf/070-060.pdf) | 76.4  | 88.8 | 72.6 | 79.2 |
