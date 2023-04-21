# Crete - Airbnb Ratings Classification Model

![img](images/seattle_readme_image.jpeg)

**Author**:

Stephanie Ciaccia

## Overview

Crete is the largest island in Greece and a popular destination known for its stunning beaches, rich history, and cuisine. The tourism industry is a major contributor to the island's economy, accounting for a significant portion of its GDP and providing employment opportunities to many local residents. 

Between January and March 2023, traffic numbers from non-European airports have increased by double digits compared to the pre-pandemic period in 2019, indicating a strong recovery in the tourism industry.

## Business Problem

The Greek National Tourism Organisation will be sharing the results of their predictive analysis of Airbnb listings with the local housing committee. The aim of this presentation is to identify the key features associated with high ratings (4 stars and above) on Airbnb listings, to assist new entrants to the Airbnb market. The objective is to offer insights and recommendations to hosts on how to enhance their listings and ultimately improve overall guest satisfaction.

## Data

- **King County Data** - I pulled the March 2023 Crete Detailed Listings data from[Insider airbnb]([http://insideairbnb.com/). Inside Airbnb is a mission driven project that provides data and advocacy about Airbnb's impact on residential communities.

The dataset includes over 30,000 entries and 74 rows of features related to the physical airbnb properties and characteristics of the hosts and reviews. It is scraped information pulled from the website. 

## Methods

I used an iterative model approach to identify the best type of classification model that should be used to predict airbnb ratings. The final model was a **decision tree** with both numerical and categorical variables. Variables include:

- home essentials (dishes and kitchen supplies)
- superhost
- host response rate
- price
- listing type
- bedrooms

I used **precision** as the main metric to determine the model's performance. The precision score helps reduce false positives while predicting ratings. This is essential as we do not want to misclassify low star properties as having high starts, as it will give airbnb hosts false expectations of an increase in bookings and reviews.

## Results

From the model, I identified four main feature with the highest feature performance:

- home essentials
- price
- host response rate

Though superhost is among the top features, since we are helping new airbnb hosts optimize their airbnb homes and listings, this is not an insightful metric to talk about as action cannot be made to change this immediately.

### Home Essentials
Home essentials and dishes (kitchen supplies) are the most important features in predicting airbnb ratings. Essential amenities are the basic items that a guest expects in order to have a comfortable stay. These include:

- Dishes
- Toilet paper
- Soap (for hands and body)
- One towel per guest
- One pillow per guest
- Linens for each guest bed

### Price
- Price is positively negatively correlated with 4 star ratings. The average nightly price for 4 star listings is **$241** compared to **$490** for homes with less than 4 star ratings.

![img](images/average_nightly_price.png)

### Host Response Rate
- The average host response rate for listings with 4 star ratings is about **20%** higher than the host response rate for listings with ratings below 4 stars.

![img](images/host_response_rate.png)


## Conclusions

As a result of this analysis, three features with the highest feature importance have been identified as the most important in classifying airbnb ratings in Crete:

- **Price**: Hosts should price their listings competitively and should reconsider nightly rates that are too high
    
- **Home Essentials**: Hosts should make sure their listings are stocked with home essentials for their stay

- **Host Response Rate**: Hosts should respond to all messages and should be timely in their responses

## Next Steps

From the initial modeling research, it is clear that the number of ratings and overall ratings play a large role in predicting whether an airbnb listing will be highly rated. To gain a more comprehensive understanding of why it would be beneficial to do further reserach into this to determine what other features are important in prediticting prices.

In addition, it would be beneficial to examine more airbnb data to improve on the class imbalance that was present and corrected by adjusting the weight of the target variables.

## For More Information

See the full analysis in the [Jupyter Notebook](https://github.com/stephcia/crete-airbnb-classification-model.git)

## Repository Structure

```
├── data
    ├──archive
├── images
├── .gitignore
├── crete_airbnb_ratings.ipynb
├── crete_airbnb_ratings_presentation.pdf
├── LICENSE
└── README.md
