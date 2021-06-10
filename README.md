# arghya05-arghya05-END2.0_Session-6
﻿# 06 Encoder Decoder

## Assignment

1.  Take the last code (+tweet dataset) and convert that in such a war that:
    1.  _encoder:_ an  RNN/LSTM  layer takes the words in a sentence one by one and finally converts them into a single vector.  **VERY IMPORTANT TO MAKE THIS SINGLE VECTOR**
    2.  this single vector is then sent to another RNN/LSTM that also takes the last prediction as its second input. Then we take the final vector from this Cell
    3.  and send this final vector to a Linear Layer and make the final prediction.
    4.  This is how it will look:
        1.  embedding
        2.  _word from a sentence +last hidden vector ->_ encoder  _-> single vector_
        3.  _single vector + last hidden vector -> decoder -> single vector_
        4.  _single vector -> FC layer -> Prediction_
2.  Your code will be checked for plagiarism, and if we find that you have copied from the internet, then -100%.
3.  The code needs to look as simple as possible, the focus is on making encoder/decoder classes and how to link objects together
4.  Getting good accuracy is NOT the target, but must achieve at least  **45%**  or more
5.  Once the model is trained, take one sentence, "print the outputs" of the encoder for each step and "print the outputs" for each step of the decoder. ←  **THIS IS THE ACTUAL ASSIGNMENT**

The Dataset consists of `1341 (Cleaned)` Tweets which are labelled `[Negative, Positive, Neutral]`
```
Negative: 931, Positive: 352, Neutral: 81
```
68% is Negative, so the model is learning
Highest Test Accuracy: `81.33%`
Epochs: `5`

Observations
- The accuracy was really high, even with just 16 dims, beacuse of less data and prone to overfitting
- Other Embedding needs to be tired , which will effect accuracy (fastetxt, word 2 vec etc)
- The dataset is relatively small,   also there is class imbalance, huge, imbalance. SMOTE and sampling needs to be tried 
- The embedding was trained on 6B texts, and has a dimension of `300`, so needs to try with other smaller dimension which would increase model performance 
- Endoder decoder is not good with long text , as encoder,decoder is slow 
