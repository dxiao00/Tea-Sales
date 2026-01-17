# Tea-Sales
Bayesian models for predicting future green tea and milk tea sales.

I work at a restaurant where one of my responsibilities is to make tea orders as they come in. 
There are two main types of tea: green tea and milk tea. Green teas are made by mixing fruit
syrups with jasmine tea and shaking with ice. While different green tea orders may ask for 
different syrups, they all require the same amount of jasmine tea. As such, it would be useful 
to know about how many green tea sales we should expect to make per day to meet customer demand,
reduce wait times, and minimize waste. 

Unlike green teas, milk teas don't share a common base ingredient, with different types requiring
different powders and syrup concentrations. Hence, it would be useful to know about how many sales
of each type of milk tea we should expect to make to ensure we have enough inventory. 
Since daily sales of any individual milk tea is relatively low, it seems much less wasteful to make
them as orders come in, so we looked at data on a weekly, rather than daily, basis.  

I created a negative binomial regression model to predict daily green tea and milk tea (all types combined)
sales. With an average prediction error of about 3.375 sales, it provides a reasonable estimate
for future tea sales. Using the model predictions for green tea sales, we reduced the occurence
of restocking events (where customers need to wait for new tea to be made) by 20% and reduced
waste/spoilage by around 37.78% compared to our baseline strategy. 

I created a hierarchical Poisson regression model to predict weekly sales for each type of milk tea. 
The model predictions were fairly accurate, with an average error of only about 3.6 sales. Around
95.3% of observations fell within their 95% prediction intervals, so using the upper intervals
provides a good guide for the stocking of ingredients. 
