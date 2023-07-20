# bird_recognition

### ml model to recognize the species of birds by their sound

our data consistent of recording of different bird species and our task is to be  able to recognize them .
the data is transformed into different shapes includes Mel spectrograms and MFCC spectrograms and bunch of other features .


![Screenshot_(39)](https://github.com/Zeromeam/bird_recognition/assets/102630502/f0e63a40-6bb5-4b50-a9d6-becb0c0cd766)

### then we searching for correlation and redundancy using pandas.
![features_labeel_corr](https://github.com/Zeromeam/bird_recognition/assets/102630502/4f6e9c6b-bdf8-459b-9725-099519a9b510)

becase the data is unbalanced i choose an evalution criterion "Macro-averaged F1" score (computed per class, then averaged) .\
$i$  ...  is the category  \
$$F_{1,i} = \frac{2\left ( prec.recall \right )}{prec+recall }$$
where :
$$recall = \frac{TP}{TP+FN}$$
$$prec = \frac{TP}{TP + FP}$$

After that we start doing cross validation using different ml algorithm and different model I was responsible for the neural network algorithm and tried FNN CNN RNN and finally MNN by entering the three Mel spectrogram that we have in a three channel 2D_CNN and the 9 MFCC spectrograms in  a 9 channel 2D_CNN and the other feature in a 1D_CNN then I  concatenated those into a FNN and that model give me the best result with the fastest convergence. 

![MMN_strc_2](https://github.com/Zeromeam/bird_recognition/assets/102630502/9b58d543-7e69-4dc7-b44e-b0e8fd87edad)

![MNN_avg_f1](https://github.com/Zeromeam/bird_recognition/assets/102630502/adde2334-8189-4191-bf57-d0581c81dcc9)
