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
    <li>From the 426K dataset provided, eliminated 392K records due to significant number of missing data (NaNs).</li>
    <li>There were 6% records (2,372 records) with $0 price. I decided to not include them due to the lack of a clear pattern in other features to impute or predict it reliably and may cause more errors in the training process. There are 32,496 records in the dataset left after this elimination, which still is a good amount of data that can be used for training </li>
    <li></li>
</ul>

