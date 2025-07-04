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
    <li>Dropped irrelevant columns like id, region, drive,VIN, model, size,and paint_color. There were total of 11 variables to be used in the anaolysis and modeling.</li>
    <li>Reformatted year and odometer by recmoving decimal points.</li>
    <li>In examining numerical features like price and odometer, noticed that there were records with zero entries. There were 6.8% records (2,372 records) with $0 price and 0.2% in odometer. Eliminated them due to the lack of a clear pattern in other features to impute or predict it reliably and may cause more errors in the training process. There are 32,496 records in the dataset left after deleteng these records, which still is a good amount of data that can be used for training. </li>
     <li>Price distribution is skewed to the right.Most of the values cluster toward the lower end (left side), while a long tail stretches out to higher values (right side), representing a few expensive observations like premium-priced cars </li>
    <img src="/images/price_distribution.png"/>
    <li>Examined the outliers in price and it appears that there were 1,007 outliers. Explain why eliminating outliers</li>
    <img src="/images/price_dist_boxplot.png"/>
   
</ul>

