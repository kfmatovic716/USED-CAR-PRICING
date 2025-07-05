# Practical Application of Machine Learning - WHAT DRIVES THE PRICE OF THE CAR?

<img src="/images/usedcardealership.jpg"/>

# MAIN OBJECTIVES
<ul>
    <li>To provide clear recommendations to a used car dealership as to what consumers value in a used car</li>
    <li>To  determine key factors that affect the price of a used car</li>
</ul>

# DATA SOURCE AND UNDERSTANDING
<p>Dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure the speed of processing. </p>

# DATA PREPARATION 
<ul>
    <li>From the 426,880 dataset provided, eliminated 392,012 records due to significant number of missing data (NaNs).</li>
    <li>Dropped irrelevant columns like id, region, drive,VIN, model, size,and paint_color. There were total of 11 variables to be used in the analysis and modeling.</li>
    <li>Reformatted year and odometer by recmoving decimal points.</li>
    <li>In examining numerical features like price and odometer, noticed that there were records with zero entries. There were 6.8% records (2,372 records) with $0 price and 0.2% in odometer. Eliminated them due to the lack of a clear pattern in other features to impute or predict it reliably and may cause more errors in the training process. There are 32,496 records in the dataset left after deleteng these records, which still is a good amount of data that can be used for training. </li>
     <li>Price distribution is skewed to the right. Most of the used car price values cluster toward the lower end (left side), with average price of $17K while a long tail stretches out to higher values (right side), representing a few expensive observations like premium-priced cars </li>
    <img src="/images/price_distribution.png"/>
    <li>Examined the outliers in price and it appears that there were 1,007 outliers. Majority of outliers were priced above $47K. For modeling purposes, elminated outliers. Modeling without outliers improves accuracy since it can skew the learning of models especially in regression by pulling the best-fit line or curve toward extreme values resulting to poor generalization and inflating evaluation metrics such as MSE and MAE. Removing outliers also improves variance in the model making stable model predictions and preventing overfitting. There were 31,489 records after deleting outliers. </li>
    <img src="/images/price_dist_boxplot.png"/>
    <li>Ran summary of stats after deleting outliers and noticed the minimum price was $1. Per my research, a reasonable price for a used car in US market should be no less than 2,000. Anything less than that often have serious mechanical issues, may not pass inspections, may have some repairs needed but will cost more to repair than own, salvaged or even scams. Therefore, deleted used car prices less than $2K. There were 30,330 records after this elimination.This is the final dataframe to be used in modeling. Price minimum at $2k and maximum at $47K (upper bound of data) </li>
    <img src="/images/model_price_distr.png"/>
    <li>Examined relationship of price to year and mileage (odometer).Newer models tend to be more expensive and low mileage cars were also more expensive.However, based on the correlation matrix results, the relationship is weak.</li>
    <img src="/images/price_by_year.png"/> <img src="/images/price_by_odometer.png"/> 
    <li>Examined price to condition and manufacturer. New and like new are definitely pricier. Manufacturers affect price especially manufacturers with varieties line models. Toyota, Chevrolet, Jeep for example were less expensive brands compared to GMC, RAM and FORD, which are also likely more expensive since they have more varieties models in trucks and SUVs. </li>
    <img src="/images/price_bycond_model.png"/>
    <img src="/images/price_bymanuf.png"/>
     <li>Transformed categorical data (manufacturer, condition, cylinders, fuel, title_status, transmission, type, state) via one hot encoder.</li>
</ul>

# MODELING AND EVALUATION
    Model 1: LINEAR REGRESSION
    Model 2: RIDGE REGRESSION
    Model 3: LASSO REGRESSION
    
# RECOMMENDATIONS