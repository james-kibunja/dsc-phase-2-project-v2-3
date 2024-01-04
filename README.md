# King County Houses Data Analysis 

![King_County_houses](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/imagereader.jpg)



## Project Overview

This project aims to provide actionable insights to a leading real estate firm in King County, Washington. We focus on refining property appraisals by analyzing key attributes—number of bedrooms, bathrooms, and housing condition. Our goal is to understand how strategic home renovations influence property values, arming the agency with tools to guide homeowners effectively. Through a comprehensive analysis of factors affecting home prices in the region, we aim to equip the firm with valuable resources for informed decision-making in the dynamic real estate market, covering aspects like buying, selling, and renovations. This project establishes a systematic methodology to optimize clients' return on investment amid the complexities of the local real estate landscape.

### Business Problem

The real estate agency aims to provide homeowners with strategic advice on optimizing property values based on key features such as the number of bedrooms, bathrooms, and housing condition. Currently, there is a lack of a systematic approach to offer informed recommendations, limiting homeowners' ability to enhance their return on investment during property sales. The agency seeks to develop a structured methodology to assess and communicate how specific features, particularly the number of bedrooms, bathrooms, and housing condition, influence property prices. This approach will empower the agency to guide clients effectively in making renovations that align with market demands, thereby maximizing the overall value of their properties.

### The Data

This project uses the King County House Sales dataset, which can be found [King County Dataset](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/data/kc_house_data.csv) with the description of the column names [columns description](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/data/column_names.md)

### Data Understanding and Analysis 
### Checking for relationship between price and independent variables
we can see that sqft_ living, grade, sqft_above have the highest correlation with the price.  
![the relationship between price and all other features](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/data_.jpg)
### Simple Linear Model
### Model 1
Now that we had sqft_living, it seemed to be a good predictor because it had the most linear relationship with price. We adopted it as our basis. For that, we created a simple model based on this.Our model is statistically significant overall, and explains about 49.3% of the variance in price.
![Model 1](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/simple_model.jpg)

Visualizing the simple linear model. We seae that 

![residual graphs](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/base_line_living.jpg)
### Multiple Linear Regression Mode
### model 2.
![Model 2](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/reg_mod2.jpg)

from the graph below we compare the relationship between price and the selected variables 

![comparing price and selected variables](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/house_vs_interest.jpg)

After digging deeper we found that degree of condition matters with the best giving high value on prices 

![condition against price](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/House_condition.jpg)

### model 3.
![Model 3](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/log_model3.jpg)

Multiple Linear Regression Visualization

![residual bathrooms](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/log_reg_mod.jpg)
![residual bedrooms](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/log_reg2.jpg)

Checking for equal variance (homoscedasticity) assumption

![homoscedastacity graphs ](https://github.com/JohnNkakuyia/dsc-phase-2-project-v2-3/blob/main/images/Homosc.jpg)

 ## Conclusion 
 
 For each increase of 1% in sqft_living, we see an associated increase of about 0.84% in price, therefore we conclude square feet living has an a positive effect on price

The coefficient for "bedrooms" suggests a negative relationship with the price,indicating that as the number of bedrooms increases, price tends to decrease.For each additional bedroom, holding all other variables constant, the log-transformed price decreases by approximately 0.158 units .

The coefficient for "bathrooms" suggests a positive relationship with the price,indicating that as the number of bathrooms increases, price tends to increase. as per the log model,For each additional bathroom, holding all other variables constant, the price increases by approximately 0.0352 units

on the other hands house condition should be given first priority as in the context of our analysis house condition correlation holds the strongest connection compared to the other features of interest. And the best fetching high value

