# Task4

## Task4 - Description

"In this task we will perform sequence classification. We will categorize temporally coherent and uniformly distributed short sections of a long time-series. In particular, for each 4 seconds of a lengthy EEG/EMG measurement of brain activity recorded during sleep, we will assign one of the 3 classes corresponding to the sleep stage present within the evaluated epoch."

## Task4 - Solution

The problem was a classification task. We had EEG / EMG measurements of 3 classes that were unbalanced. We used different techinques to extract features that we used for the classification. For each EEG signal using the biosspy library we extracted the energy waves bands (alpha, beta, gamma, delta and theta). For each of these waves we calculated the mean, average, standard deviation, range and energy. These features were important to distinguish before Non-REM and REM stage. Another feature that we added was Sum of the power in all five energy bands. For each EMG signal we extracted the energy, the zero-crosses and the sign changes of the singal. EMG charactirizes brain muscle activity and these features are important to distinguish if the subject is asleep or not. With RandomForest we performed feature reduction (dimensionality reduction). Using all of the remained features we trained a Support Vector Machine which was fine-tuned using Cross-validation and Leave-one-subject-out (LOSO) validation. The model has 0.93 mean score in the LOSO cross-validation and 0.9397 in the public scoreboard.

