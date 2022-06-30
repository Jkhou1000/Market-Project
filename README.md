# Understanding the properties of products and roles of the outlets that sell them
## Data Viz & Machine learning models for predictions

**Joshua Khoury**: 

### Business problem:
The current project explores the data and tries to help supermarkets or grocery stores figure out its sales
specifically what is selling and why.



### Data:
The source of this data is https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

This sheet explores things like the location, type of market, and year established among other factors about the store itself. It also goes over features such as the type of item, weight, fat content, visibility, and the sales it has made at specific locations.

## Methods
Renaming the columns for simpler coding is an important step, followed by the usual checks for duplication and NaN values
I had orginally decided to drop Item weight but I felt leaving the value at zero for the missing data would be more useful, whereas I completely dropped Outlet Size (o_size) because I felt the data was a bit too imprecise, "Medium", "High", etc does not give me much to work with in addition to missing a moderate amount of data.
I also fixed/replaced the Low Fat & Regular values because some of those are inconsistent, something noticeable even from a short read in the original csv file.

## Results
I ended up cleaning the data thouroughly and isolated important values from my Dataframe as a final touch
the min, max, and average of things like an item's weight, retail price, Item outlet sales, and visibility

I created multiple data visualizations, 2 of those mostr advanced will be outlined below with images, but most of them explore the relationship between certain features in order to make observations about the data after it was cleaned.

Finally, I created 2 machine learning models and evaluated their performance and decided on which one I thought would work better in determining the relationship between an outlet's item sales against several of the other factors I found most appropriate.

##### Item Visibility's effect on sales
![Scatterplot 1](https://user-images.githubusercontent.com/105755535/176532985-ef8719f4-0a14-4e52-9921-6b09d0e89a11.png)


>This scatterplot explores the effect an item's visbility has on its sales based on where it is sold.

##### 
![Barplot 2](https://user-images.githubusercontent.com/105755535/176514655-dfe94616-2a01-4e99-b2f7-231c66914d16.png)
>A complex barplot going over the maximum retail price for items purchased by each type of store

#### Models 

I ran 2 different models, a Regression linearity model and a Regression Tree model. after running the first one and then tuning the second I came the the conclusion that the linear regression model was better for this Dataframe. both of the R^2 scores are perfectly fit, but Regtree's MSE and RMSE indicate underfitting for its errors even after being tuned better. 

### Recommendations
Use this model to determine what items to sell at specific outlets, and see which items benefit from things like item visibility or if things like Low Fat or Regular items sell better.

### Limitations and Next steps
This is a rather simplistic overview of the data, the there were only two fitted models. The next steps would be to find and analyze more advanced data visulizations, and compare more types of models and the metrics.

### Questions & Contact

for any questions, please contact joshguy62@gmail.com
