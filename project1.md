Write a one and a half to two-page report on your results and include the following:
1. A description of the housing data you scraped from Zillow
- For Project 1, we took data from Zillow. Specifically, I looked at the Charlotte, North Carolina area. We cleaned the data through R and set up a data frame which we converted to a csv file.  The csv file included price of the home, number of beds, number of baths, and the square footage of the home. Later on, we imported the zip codes of the homes as well. In order to add the zip code to our machine learning model, we converted the numeric values into categorical values. After processing our data, there were 384 homes that had a value for these features. The summary statistics for the price of the home, the number of bedrooms, the number of baths, and the square footage is below. Looking at a histogram of our price data, we can see that our pricing data is skewed left.

![](summary_table.PNG)

2. A description of your model architecture
- The model architecture used stochastic gradient descent as the optimizer and mean squared error as the loss. The model was Sequential and used dense layers. The number of layers varied. Originally, it was three layers consisting of number of beds, number of baths, and square feet. When adding in the zip codes to our model, it increased to 29 layers. This means that there were 26 different values for the zip codes in our data. The target was the price of the home. 
3. An analysis of your model output
- The model varied in its predictions. Originally, we scaled our data by diving the price by 100,000 and the square footage by 1000. Doing improved our model’s efficiency. When the data features included the zip code, the loss decreases originally, but levels out quickly. Without the zip code, there is not much loss in
4. An analysis of the output that assesses and ranks all homes from best to worst deal
