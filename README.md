![cover](https://github.com/heathlikethecandybar/dsc-phase-2-project-v2-3/blob/main/images/cover.jpeg)

# King County Housing Analysis

**Author**: [Heath Rittler](mailto:hrittler@gmail.com)


## Overview

'The King is dead. Long live the Queen.'  

Just outside Issaquah, Washington (located in King County), there is a small real estate agency looking to differentiate themselves from their larger more experienced competitors.  The agency has figured out that a good way to differentiate themselves from their competitiion is to focus on home improvement recommendations to homeowners.  These recommendations coupled with a personal relationship, they belive will optimize the buying and selling of the homes.


## Business Problem

For these receommendations, I have been inlisted to help decipher which home improvements lead to the value of a home.  The output of my analysis will show at least 2 features that will impact the value of a home to get them started.  Each one of these features should be in control of the homesowner, meaning they will be able to make those changes if they so desire before listing their home.  For this project, I used a multivariate linear regression model to analyze house sales in King County, Washington.


## Data

This project uses the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this repository. The description of the column names can be found in `data_dictionary.md` in the same folder.  The dataset includes 21,597 entries, and 21 columns.  Here are the columns in the dataset:

* `id` - Unique identifier for a house
* `date` - Date house was sold
* `price` - Sale price (prediction target)
* `bedrooms` - Number of bedrooms
* `bathrooms` - Number of bathrooms
* `sqft_living` - Square footage of living space in the home
* `sqft_lot` - Square footage of the lot
* `floors` - Number of floors (levels) in house
* `waterfront` - Whether the house is on a waterfront
* `view` - Quality of view from house
* `condition` - How good the overall condition of the house is. Related to maintenance of house.
* `grade` - Overall grade of the house. Related to the construction and design of the house.
* `sqft_above` - Square footage of house apart from basement
* `sqft_basement` - Square footage of the basement
* `yr_built` - Year when house was built
* `yr_renovated` - Year when house was renovated
* `zipcode` - ZIP Code used by the United States Postal Service
* `lat` - Latitude coordinate
* `long` - Longitude coordinate
* `sqft_living15` - The square footage of interior housing living space for the nearest 15 neighbors
* `sqft_lot15` - The square footage of the land lots of the nearest 15 neighbors

Additional information about this dataset can be found on the [King County Assessor Website](https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r) Accessor Website. 


## Methods

The project uses multivariate linear regression model to analyze house sales in King County, Washington.  Out dependent variable, 'price', is what we are trying to optimize for in order to give the best recommendations.  We will be trying to optimize our r2 values, however, we are not necessarily trying to predict home values, we are just trying to infer what variables will give home owners the best bang for their dollar -- not necessarily a ROI on that investment.  In addition, we will be removing any features that have a p-value of > 0.05 to optimize for any error within our variables.


## Results

The first view we took was looking at our average and median price for homes over time.  The dataset has a pretty broad range of homes, starting in 1990 all the way until 2015.  Being that we are focusing on more r
To normalize the data, we began our analysis by pulling only the records from 1990 and after.  This gives us a much more normal distribution of price data, giving us better result when we look at our model's performance. 

The median home value for King County during this time period is $475k.  So homeowners will quickly be able to assess where the perceived value of their home stands in comparison. This to say that houses with this median home value, also have 2,240 square foot of living area, 3 bathrooms, and an median grade number of 8.  Which are features we will continue to evaluate in our model as impactable features.
![median_home_value_over_time](https://github.com/heathlikethecandybar/dsc-phase-2-project-v2-3/blob/main/images/median_home_value_over_time.png)


![sq_ft_price_scatter](https://github.com/heathlikethecandybar/dsc-phase-2-project-v2-3/blob/main/images/sq_ft_price_scatter.png)

![baths_round_hbar](https://github.com/heathlikethecandybar/dsc-phase-2-project-v2-3/blob/main/images/baths_round_hbar.png)

## Conclusions

This analysis leads to three recommendations for the improvement of home value:

- **By increasing the living square footage of your home, you can increase the value by $99 per square foot.** 
- **By adding bathrooms, and adding 1/4 bath features, you can increase the value of your home by $22k for each 1/2 bath you add.** 

## Moving Forward

Further analyses could yield additional insights to further improve success at Microsoft:

- **Look at additional zip codes to understand values more specifically (or not)** 
- **Evaluate additional variables/ features such as environmental, or other factors that may have an impact on a home’s value**
- **3**


## For More Information

The full analysis is located in the [Jupyter Notebook](./phase_2_project.ipynb) or review this summary [presentation](link).

For additional info, contact Heath Rittler at [hrittler@gmail.com](mailto:hrittler@gmail.com)


## Repository Structure

```
├── data
├── images
├── README.md
├── FI - Phase 2 Project.pdf
└── phase_2_project.ipynb
```


cover photo credit:  King Country, Washington - Government Facebook Page https://www.facebook.com/photo/?fbid=478811227612794&set=a.298803398946912