# Atrial Fibrillation Classification from short ECG (CINC 2017 Challenge)

This project is inspired from CINC challenge which is aimed to encourage the development of algorithms to classify, whether short single lead ECG recordings (between 30 s and 60 s in length) show normal sinus rhythm, atrial fibrillation (AF), an alternative rhythm, or is too noisy to be classified. 


![Figure 1. Example of the ECG waveforms](figures/example_waveforms.svg)

In this project, we will start by building a simpler two-class classifier distinguishing between normal sinus rhythm and abnormal rhythm (atrial fibrillation included) by excluding the noisy recordings. We will thus use 7,418 out of the original 8,528 training data recordings. They have been converted into 'npz' format from the original MATLAB V4 WFDB-compliant format. 

We will perform the following 
1. Even though, RR intervals are already provided, we will first build an algorithm to extract RR intervals using the Pan-Tompkins method and measure the accuracy performance of our algorithm.
2. We will then process and extract features from the RR intervals data for our classifier.
3. Build and compute the performance of a 2-class random forest classifier

We will eventually take the challenge of 
1. Performing a grid search for hyperparameter tuning
2. Comparing different classifiers
2. Distinguishing between AF from alternative rhythm. This most likely will require extracting features other than RR intervals data, such as the presence/absence of P-wave.
 
 
