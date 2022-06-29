# Understanding the properties of products and roles of the outlets that sell them
## Data Viz & Machine learning models for predictions

**Joshua Khoury**: 

### Business problem:
The current project explores the data and tries to help supermarkets or grocery stores figure out its sales
specifically what is selling and why.



### Data:
The source of this data is https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/
This sheet explores things like the location and type of market an item is being sold at and the opening year 
as well as the type of item, its weight, fat content, and the sales it has made at specific locations



## Methods
Renaming the columns for simpler coding is an important step, followed by the usual checks for duplication and NaN values
I had orginally decided to drop Item weight but I felt leaving the value at zero for the missing data would be more useful, whereas I completely dropped Outlet Size (o_size) because I felt the data was a bit too imprecise, "Medium", "High", etc does not give me much to work with in addition to missing all that data
I also fixed/replaced the Low Fat & Regular values because some of those are inconsistent, and its noticeable even from a short read in the original csv file.

## Results
I ended up cleaning the data thouroughly and isolated important values from my Dataframe as a final touch
the min, max, and average of things like an item's weight, retail price, Item outlet sales, and visibility

I created multiple data visualizations, 2 of which will be outlined below with images, and finally, I created 2 machine learning models and evaluated their performance and decided on which one I thought would work better.



##### Item Visibility's effect on sales
![Scatterplot 1](https://user-images.githubusercontent.com/105755535/176532985-ef8719f4-0a14-4e52-9921-6b09d0e89a11.png)


>This scatterplot explores the effect an item's visbility has on its sales based on where it is sold.

##### 
![Barplot 2](https://user-images.githubusercontent.com/105755535/176514655-dfe94616-2a01-4e99-b2f7-231c66914d16.png)
>A more complex barplot going over the maximum retail price for items purchased by each type of store

## Linear Regression vs Regression Trees

Both of the models have issues, they have only a moderate R2 averaging around 50-60 which means an error variance of around 40% and they have high RSME which means errors in the thousands.
Both of the R2 are pretty close, so this means both are fitted well, the Regression tree one a little more so after its tuning.

After comparing these 2 and moderate deliberation, I decided the Regtree one was more fitting, literally!
The Regression tree is slightly more apart in its score than the Line Regression model, but not by a signifcant degree which gives you a stronger 60% on its trained data. its RMSE is both lower than the LineReg's model as well as closer together on train & test than Line's which means the margin for error is lesser as well.

I've put below the 2 most important metrics from the training and test side of both which I went over above
#### **RegTree important metrics (from the tuned depth 5 model)**
- Dectree5 R2 Training: 0.6 
- Dectree5 R2 Training: 0.59
- DecTree5 Train RMSE: 1082.7121818891044 
- Dectree 5Test RMSE: 1057.5149155444085

I believe the model would work decently for the purposes of this problem but it could use more tuning than is unavailabe from either of these models. The RMSE error is off by thousands and that can make for some missteps since it refers to the Item outlet sales range from 0-12000 and the R2 score denotes that there's about a 40% error variance.

## Recommendations:



## Limitations & Next Steps
There could be more model testing done on the values for starters, and my ability to tune is somewhat limited in general. The next steps would be to compare more models or tune the Regression tree further. I could also add more data visualizations and explore further types of graphs


### For further information


For any additional questions, please contact **joshguy62@gmail.com**
