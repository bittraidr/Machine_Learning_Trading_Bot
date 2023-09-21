# Machine_Learning_Trading_Bot
UC Berkeley Fintech: Develop a machine learning trading algorithm.


## What impact resulted from increasing or decreasing the training window?

Decreasing the training window from 3 to 1 month actually made the strategy returns line graph higher then the actual returns. The precision and recall for the sell indicator -1 decreased from .43 precision to .37 and recall of .04 to .03 from 3 months to 1 month. So we lose a small amount of precision and recall with the dateoffset(month=1) from dateoffset(month=3). Everything else including accuracy remainded largely the same. 

Increasing the training window from 3 to 6 months saw shows a small change in precision and recall of -1 with an increase from .43 to .44 precision and a decrease from .04 to .02 recall. The 1 row precision stayed the same however the recall for 1 increased from .96 to .98 and the accuracy increased from .55 to .56. The graph changed a bit from 2019 to 2021 for the 6 month compared to 3 month with the 6 month showing a bit more volatility with lower lows and higher highs than the 3 month window. 



## What impact resulted from increasing or decreasing either or both of the SMA windows?





