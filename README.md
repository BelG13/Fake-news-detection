# Fake-news-detection
 Machine Learning project : Build the best model in order to predict if a given news is fake or not.
 
The initial version of this project uses a passive agressive algorithm.
I may update this project more or less often , so that we can see perfomances for many model instead of just the passive agressive one.


Structure : 

### I/ Data cleanning :

    very fast , the dataset is almost fully prepared.
    • dataset's import
    • split test and train data
    • apply tfidf_vectorizer on features

### II/ Model selection :

    1 - Passive Agressive model
        • print global result about pas-classifier (cross_val_score , confusion matrix)
        • GridSearchCV in order to find the best tune
        • ROC and ROC-AUC 
            => I chose ROC instead of precision/recall metrics because I care a lot more about 
               'FAKE' classified as 'REAL' than 'REAL' classified as 'FAKE'.
               I prefer minimize 'FAKE' classified as 'REAL' even if it means that I have to classify 
               more often 'REAL' news as 'FAKE'.
            => use the ROC curve to choose a good threshold
        • display the confusion matrix with the nex threshold
        • display the predicted label and the test label in a confusion matrix (with my new treshold)

    2 - Random Forest Trees ?
 
