
# Sports Persion Classification

In this project i made a Classification model which classify the sport
person with their image.We restrict classification to only 5 people :-  

    1. Maria Sharapova
    2. Serena Williams
    3. Virat Kohli
    4. Roger Federer
    5. Lionel Messi     

Technologies used in this project :-    

    1. Python
    2. Numpy and OpenCV for data cleaning
    3. haar cascade - detect face and eyes
    4. Matplotlib & Seaborn for data visualization
    5. Pywavelet
    6. Sklearn for model building
    7. Jupyter notebook

- detect face and eyes of image with the help of opencv. We use 
    haar cascade for that.
- crop the facial region of image    
- then use wavelet transform for training our model.In wavelet transformed image, you can see edges clearly and that can give us clues on various facial features such as eyes, nose, lips etc  
- load the image detect face and eyes. if eyes>=2 then save and crop the face region.   
- Data Cleaning is done. Now we train the model with the help of sklearn features
  we use svm for that.
- Classification Report :-  

                precision     recall   f1-score   support

           0         0.67      1.00      0.80         4
           1         0.43      1.00      0.60         3
           2         1.00      0.20      0.33         5
           3         0.00      0.00      0.00         2
           4         1.00      1.00      1.00         1
        accuracy                         0.60        15   
        macro avg    0.62      0.64      0.55        15
        weighted avg 0.66      0.60      0.51        15
- Now use GridSearch to try out different models with different paramets. Goal is to come up with best modle with best fine tuned parameters.
-       model	                   best_score      	best_params 
         0	svm             	0.583333	{'svc__C': 1, 'svc__kernel': 'linear'}
         1	random_forest	        0.541667  	{'randomforestclassifier__n_estimators': 10}
         2	logistic_regression	0.602778	{'logisticregression__C': 1}    

- draw the confusion matrix using Seaborn for better understanding.
- save the model using joblib.


