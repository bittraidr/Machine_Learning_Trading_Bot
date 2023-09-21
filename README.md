# Machine_Learning_Trading_Bot
UC Berkeley Fintech: Develop a machine learning trading algorithm.


## What impact resulted from increasing or decreasing the training window?

Decreasing the training window from 3 to 1 month actually made the strategy returns line graph higher then the actual returns. The precision and recall for the sell indicator -1 decreased from .43 precision to .37 and recall of .04 to .03 from 3 months to 1 month. So we lose a small amount of precision and recall with the dateoffset(month=1) from dateoffset(month=3). Everything else including accuracy remainded largely the same. 

Increasing the training window from 3 to 6 months saw shows a small change in precision and recall of -1 with an increase from .43 to .44 precision and a decrease from .04 to .02 recall. The 1 row precision stayed the same however the recall for 1 increased from .96 to .98 and the accuracy increased from .55 to .56. The graph changed a bit from 2019 to 2021 for the 6 month compared to 3 month with the 6 month showing a bit more volatility with lower lows and higher highs than the 3 month window. 



## What impact resulted from increasing or decreasing either or both of the SMA windows?

Decreasing both SMA windows, the short window from 4 to 2 and the long window from 100 to 50 kept the strategy returns aligned with the actual returns longer. Increasing the short window from 4 to 8 and the long from 100 to 200 performed worse on the graph with the strategy line dropping well below the actual returns. 



## Did this new model perform better or worse than the provided baseline model? 

The new Logistic Regression model performed better in all areas including the graph. the -1 precision is up from .43 to .88 with the new LR model. Also with 1 buy precision went from .56 with the first model to .65 with the new LR model. Recall jumped up from .04 precision and .96 recall to .14 and .99 respectivelly. The accuracy also jumped from .55 to .66 with the new LR  model. The graph saw some inital decline in performance around 2016 then noticable gains from 2019 to 2021 in comparision to the origional model. 

## Did this new model perform better or worse than your tuned trading algorithm?