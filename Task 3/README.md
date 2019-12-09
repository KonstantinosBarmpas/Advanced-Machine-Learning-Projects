# Task3

## Task3 - Description

"While the previous projects dealt with medical image features, we turn now to the classification of entire time series into one of 4 classes. This time you will work with the original ECG recordings of different length sampled as 300Hz to predict heart rhythm."

## Task3 - Solution

The problem was a classification task. We had ECG measurements of 4 classes that were unbalanced and of not the same length. We used different techinques to extract features that we used for the classification. For each ECG signal we extracted the autocorrelation, the average and the power. We also extracted 15 coefficients of the FFT. For each ECG using biosspy we extracted the heartbeats, averaged them and created a characteristic average of the same length of each patient. For each of these signals (after normalization) we extracted the energy of the wave, the T, S, P, R, Q peaks, the ST QRS PR intervals, QRS/T and QRS/P ratios, the median, mean and interval of the amplitude and the db2 coefficients. Finally, the library biosspy gave us the locations of peaks in the original wave, the timings as well as the heart beats and their timings. For all of them we calculated the mean, median and standard deviation. We also extracted the mean, median and standard deviation of the differences between the peaks' timings( important feature to classify noise, normal heart rate and abnormal heart rhythms). Using all of these features we trained a GradientBoosting model which was fine-tuned using a Cross-validation grid search. The model has 0.817 mean score in the cross-validation and 0.833 in the public scoreboard.

