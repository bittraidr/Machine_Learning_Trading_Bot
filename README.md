# Machine_Learning_Trading_Bot
UC Berkeley Fintech: Develop a machine learning trading algorithm.


## What impact resulted from increasing or decreasing the training window?


Decreasing the training window from 3 to 1 month actually made the strategy returns line graph higher than the actual returns consistently. The precision and recall for the sell indicator -1 decreased from .43 precision to .37 and recall of .04 to .03 from 3 months to 1 month. So we lose a small amount of precision and recall with the dateoffset(month=1) from dateoffset(month=3). Everything else, including accuracy remained largely the same. 

Increasing the training window from 3 to 6 months saw shows a small change in precision and recall of -1 with an increase from .43 to .44 precision and a decrease from .04 to .02 recall. The 1 row precision stayed the same, however the recall for 1 increased from .96 to .98 and the accuracy increased from .55 to .56. The graph changed a bit from 2019 to 2021 for the 6 month compared to 3 months with the 6-month showing a bit more volatility with lower lows and higher highs than the 3-month window. 



## What impact resulted from increasing or decreasing either or both of the SMA windows?



Decreasing both SMA windows, the short window from 4 to 2 and the long window from 100 to 50 kept the strategy returns aligned with the actual returns longer. Increasing the short window from 4 to 8 and the long from 100 to 200 performed worse on the graph, with the strategy line dropping well below the actual returns. Increasing the SMA short to 8 and the SMA long to 150 didn't have any notable effect on the precision, recall, and accuracy.  




## Did this new model perform better or worse than the provided baseline model? 


The new Logistic Regression model performed later in the dataset from the tuned model when comparing the graphs, however the tuned model seemed to offer high strategic returns earlier and more consistently. The sell (-1) precision is up from .43 to .88 with the new LR model. Also with buy (1), precision went from .56 with the first model to .65 with the new LR model. Recall jumped up from .04 precision and .96 recall to .14 and .99 respectively. The accuracy also jumped from .55 to .66 with the new LR model. The graph saw some initial decline in performance around 2016 then noticeable gains from 2019 to 2021 in comparison to the original model. 

## Did this new model perform better or worse than your tuned trading algorithm?


The new Logistic Regression model performed better later in the dataset and showed higher strategic returns opportunities, however the tuned 1-month model seemed to show consistent higher strategic returns from the first half of the graph performing better then the Logistic Regression model in that regard.  The new LR model shows improvements in precision, recall, and accuracy noted below the original model. 

### Tuned Model Window 6 month

   precision    recall  f1-score   support

    -1.0       0.44      0.02      0.04      1732
     1.0       0.56      0.98      0.71      2211

    accuracy                           0.56      3943
   macro avg       0.50      0.50      0.38      3943
weighted avg       0.51      0.56      0.42      3943


### Tuned SMA Short = 2 SMA Long = 75
   precision    recall  f1-score   support

     -1.0       0.49      0.05      0.09      1734
     1.0       0.56      0.96      0.71      2218

    accuracy                           0.56      3952
   macro avg       0.52      0.50      0.40      3952
weighted avg       0.53      0.56      0.44      3952


### Tuned Model 1 month window 
  precision    recall  f1-score   support

        -1.0       0.37      0.03      0.06      1828
         1.0       0.56      0.96      0.70      2324

    accuracy                           0.55      4152
   macro avg       0.47      0.49      0.38      4152
weighted avg       0.48      0.55      0.42      4152


### New Logistic Regression Model

 precision    recall  f1-score   support

    -1.0       0.88      0.14      0.25        49
    1.0       0.65      0.99      0.78        79

    accuracy                           0.66       128
   macro avg       0.76      0.57      0.51       128
weighted avg       0.74      0.66      0.58       128