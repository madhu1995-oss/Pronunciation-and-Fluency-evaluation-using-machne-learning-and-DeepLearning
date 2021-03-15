

 


## Version 0
### Fluency
1.Extracted various features such as mfccs,,zero-crossing rate, spectral flux, root mean square energy from audio data set \
2.Then used various machine learning (SVM, RF,) and Deep Learning(MLP, CNN, RNN) for classification which is then trained on 70 percent data and 30 percent for test.\
3.The random forest seemed to perform better because even though for other models accuracy was high for the test set, it has high false positive and false negative, whereas for random forest only 4 samples FP and FN
### Pronunciation
When a person pronounces incorrectly then the spectrogram  of that word will be different from the spectrogram of actual pronunciation of the same  word.One can calculate the difference between the two to know if he/she has pronounced incorrectly.
### Grammatical errors
***By converting speech to text***\
1.Covert from speech to text with autocorrection \
2.Convert the text output to speech \
3.Find the dynamic time warp similarity using fast dynamic time warp algorithm.\
4.If the difference is more than a thresold then the word is mispronounced.
## Version 1 
***This will neither  require seperate methods for pronunciation and grammatical errors nor require conversion from speech to text***\
1.Convert the actual texts and perturbed texts to speech let's say speech_actual and speech_perturbed.\
2.Train sequence to sequence  model using speech_perturbed as input and speech_actual as output.\
3.In order to handle two same sentence but with different sequence lenght dynamic time warping or similar method can be used .\
4.When the user inputs incorrect voices then the system will correct voices without converting to text.\
5.Once can calcuate the similarity or difference score betwen input voice and corrected voice by using sequence correlation coefficient.
## Version 3
One can use iterative learning where the models are trained continousy and also can use federated learning  where training will happen on their device so that there is no issue of data privacy.
