## Assumption:
**This will not consider fluency into account since it is not neccessary that a person who is proficient should be fluent**.
 


## Version 0
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
