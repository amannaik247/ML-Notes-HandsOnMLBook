# How to select models?

- Before diving deep into a single model and hyper param tuning, first pick some potentially good models for the task and test them. Goal is to short list potentially good models(2 to 5).

# Search CV

### GridSearchCV

- Uses a set of given list of pramas and considers every hyper param for trianing

### RandomSearchCV

- Uses a range of params (it will pick any randomly) and you can specify how many iterations to work on

# Tip : For getting important features

The sklearn.feature_selection.SelectFromModel transformer can automatically drop the least useful features for you: when you fit it, it trains a model (typically a random forest), looks at its feature_importances_ attribute, and selects the most useful features. Then when you call transform(), it drops the other features.

# Analysing the best models and their errors

- Note: The search.best_estimator_ gets the best model but also has preprocessing with it so you dont have to preprocess the test data. Because when to do .fit() it will do preprocessing as well.
