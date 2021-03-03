
1.From the  texts of BookCorpus Or wikipedia,apply random perturbations such as \
i)Subtraction of articles \
ii)Subtraction of second part of a verb contraction(eg “ve”,”ll”,”s”,”m”)\
iii)Replace  helping verbs  e.g “am ” with “are” to check for subject verb agreement such as “Neither you nor I am  good at it” and “Neither you nor I are  good at it”.\
2Train sequence to sequence model with incorrect sentence as input and correct sentence as output.In this way the model will learn to correct grammatical errors.\
3)Train another model to covert speech to text.\
4)During testing ,speech is converted to text ,the incorrect text is then corrected using the previous model.We are using model for correction because during testing.\
we will not have correct sentence from where one can verify unlike other problems.\
5)Similarity score is calculated between input sentence and the corrected output sentence to detect the errors.
