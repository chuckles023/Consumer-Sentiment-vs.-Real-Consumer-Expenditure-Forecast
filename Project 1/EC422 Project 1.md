Consumer Sentiment vs. Real Consumer Expenditure Forecast

February 2, 2024

Recently we have seen a major surge in the consumer sentiment index, as reported by the University of Michigan Consumer Sentiment index, but how will this affect real consumer spending?  The level of consumer sentiment is still a ways away from its pre pandemic highs, but we have seen a 29% increase since November of last year.  Before this unexpected surge, consumers were down on the economy because of high inflation and fears of recession.  With inflation down consumers are much more happy with the outlook of the economy.  In the past, many economists have attempted to use UMCSENT as a predictor of economic activity but have not found a significant relationship.  The question is, can we pull useful information from a consumer sentiment index and how does UMCSENT compare to other indexes of similar purposes.  

One such comparable index would be the Conference Board’s Consumer Sentiment Index as mentioned in the New York Fed.  While UMCSENT has more data dating back to the 1940’s, the Conference Board’s Index has more explanatory power for several categories of consumer spending.  Both surveys ask 2 questions about consumers’ present conditions and 3 about their expectations for the near future.  UMCSENT’s questions pertain to changes in the economy as a whole versus economic activity.  The Conference Board’s questions ask more about employment and business conditions, which reflect differently on economic activity.  We see these differences in survey questions present themselves when each index peaks.  UMCSENT peaks when economic growth is high, while the Conference Board peaks when unemployment is low.  From this comparison we see that while UMCSENT is an index that provides useful information on consumers' feelings it does not necessarily relate to their behavior due to outside influences.  

For example, we can look at how major American events like a presidential election have an effect on consumer sentiment.  Because of factors like inflation and gas prices, President Biden’s approval rating is low, so it might be helpful to look at how consumers were behaving post-2016 election when Donald Trump was originally elected.  Immediately after Trump was elected, republicans became much more optimistic relative to democrats, according to the Survey of Consumer Expectations from the FED.  We also saw that republican counties were more pessimistic relative to democrats leading up to the election.  There are a few obvious differences between these 2 demographics, like average education and mean household income, but it was found that they didn’t have a significant effect on the difference in sentiment.  If we believe that consumers will react to the election similarly to 2016, it would be reasonable to believe that consumer sentiment will go even higher post election and is actually at a lower point right now.  

**Method:**

In my analysis I take into account variables, UMCSENT and PCEC96.  UMCSENT is the aforementioned University of Michigan Consumer Sentiment index while PCEC96 is a measure of personal consumption expenditures.  Computing a regression of these two variables can give us somewhat of an idea of how consumer sentiment will match up with how a person will spend over the course of a year.  Looking at the data from a visual standpoint we can see that consumer sentiment takes larger dips from major events like the 2008 recession and the pandemic in 2022 compared to personal consumption expenditures.  

**Graphs of UMCSENT and PCEC96 over time:**  
![][images/imageproject1_1.png]

Linear Regression \- Estimation by Least Squares  
Dependent Variable PCEC96  
Monthly Data From 2002:01 To 2023:12  
Usable Observations                       204  
Degrees of Freedom                        202  
Skipped/Missing (from 264\)                 60  
Centered R^2                        0.0058113  
R-Bar^2                             0.0008895  
Uncentered R^2                      0.9883369  
Mean of Dependent Variable       12799.067157  
Std Error of Dependent Variable   1397.913062  
Standard Error of Estimate        1397.291185  
Sum of Squared Residuals         394389376.30  
Regression F(1,202)                    1.1807  
Significance Level of F             0.2785015  
Log Likelihood                     \-1765.8858  
Durbin-Watson Statistic                0.0120

    Variable                        Coeff      Std Error      T-Stat      Signif  
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*  
1\.  Constant                     12160.627347   595.637633     20.41615  0.00000000  
2\.  UMCSENT                          8.015566     7.376632      1.08662  0.27850151

![][imageproject1_2.png]

**Conclusion:**

	After running a regression of the log difference of personal consumption vs consumer sentiment, there is a trend in the data with a coefficient of 8, but because the scale is in the 10’s of thousands it is a minimal effect.  In an attempt to forecast how personal consumption would change in January 2024, the model would not give us much if any information on how we would expect our clients' sales to perform.  The scatter shows this more clearly with an r-squared of .01 and a very flat slope.  This means that while we are seeing a boom in consumer sentiment, on the whole we can’t use this as a precise indicator of an increase in real consumption.  When looking at the graph of personal consumption we see outlying data during the pandemic with the graph taking a very large dip, but this doesn’t do much to help the correlation because consumer sentiment follows a completely different trend.  This could be due to how the University of Michigan Survey is set up.  The New York Fed article mentions that sentiment is highest during times of rapid growth in the economy which is relative compared to how the economy is doing overall.  It might be best to find an index that poses questions that will give a better outlook on how people feel in the context of a wider range of time.  When looking at the variables, we can see that personal consumption expenditures is a basic upward sloping curve with small hiccups during recessions, so it could be strongly correlated with overall inflation, while consumer sentiment is much more volatile and reactive to current events, for example the presidential elections.  While we believe that the economy is heading in a positive direction with inflation down and sentiment up, I believe that there is not enough evidence that real consumer spending will increase.    

**Sources:**

1. [**https://www.newyorkfed.org/medialibrary/media/research/epr/98v04n2/9806bram.pdf**](https://www.newyorkfed.org/medialibrary/media/research/epr/98v04n2/9806bram.pdf)

2. [**https://libertystreeteconomics.newyorkfed.org/2017/12/political-polarization-in-consumer-expectation/**](https://libertystreeteconomics.newyorkfed.org/2017/12/political-polarization-in-consumer-expectation/)

3. [**https://www.wsj.com/economy/consumers/americans-are-finally-feeling-better-about-the-economy-e964804f?mod=Searchresults\_pos1\&page=1**](https://www.wsj.com/economy/consumers/americans-are-finally-feeling-better-about-the-economy-e964804f?mod=Searchresults_pos1&page=1)

