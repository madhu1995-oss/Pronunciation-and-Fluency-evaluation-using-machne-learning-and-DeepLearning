## Assumption:
**This will not consider fluency into account since it is not neccessary that a person who is proficient should be fluent**.
 


## Version 0
### Pronunciation
When a person pronounces incorrectly then the spectrogram  of that word will be different from the spectrogram of actual pronunciation of the same  word.One can calculate the difference between the two to know if he/she has pronounced incorrectly.
### Grammatical errors
***By converting speech to text***\
1.From the  texts of BookCorpus Or wikipedia,apply random perturbations such as \
i)Subtraction of articles. \
ii)Subtraction of second part of a verb contraction(eg “ve”,”ll”,”s”,”m”).\
iii)Replace  helping verbs  e.g “am ” with “are” to check for subject verb agreement such as “Neither you nor I am  good at it” and “Neither you nor I are  good at it”.\
2Train sequence to sequence model with incorrect sentence as input and correct sentence as output.In this way the model will learn to correct grammatical errors.\
3)Train another model to covert speech to text.\
4)During testing ,speech is converted to text ,the incorrect text is then corrected using the previous model.We are using model for correction because during testing.\
we will not have correct sentence from where one can verify unlike other problems.\
5)Similarity score is calculated between input sentence and the corrected output sentence to detect the errors.
## Version 1 
***This will neither  require seperate methods for pronunciation and grammatical errors nor require conversion from speech to text***\
1.Convert the actual texts and perturbed texts to speech let's say speech_actual and speech_perturbed.\
2.Train sequence to sequence  model using speech_perturbed as input and speech_actual as output.\
3.In order to handle two same sentence but with different sequence lenght dynamic time warping or similar method can be used .\
4.When the user inputs incorrect voices then the system will correct voices without converting to text.\
5.Once can calcuate the similarity or difference score betwen input voice and corrected voice by using sequence correlation coefficient.
## Version 3
One can use iterative learning where the models are trained continousy and also can use federated learning  where training will happen on their device so that there is no issue of data privacy.
