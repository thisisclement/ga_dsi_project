# Project 2: Ames Housing Predictor Model

Author: Clement Ow


### Contents:
- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Data Dictionary](#Data-Dictionary)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Problem Statement

Predictors of housing prices can vary from state to state. With 70 over possible predictors, find out the top five predictors that can highly influence housing prices.

## Executive Summary

There are too many possible indicators that might drive up or down housing prices. In this beautiful city of Ames, there are 70 over possible indicators that can influence housing prices. This information can help inform buyers to look for the right kind of feature in a house or even help home owners and property companies better price them. With the right kind of predictors, this model aims to make the property market in Ames a fair and competitive one that will benefit both buyers and sellers.

## Data Dictionary

Data dictionary for the final set of features.

| Feature           | Type  | Description                                                                                    |
|-------------------|-------|------------------------------------------------------------------------------------------------|
| 1st Flr SF        | int   | First Floor square feet                                                                        |
| Bsmt Exposure     | int   | Refers to walkout or garden level walls                                                        |
| Bsmt Full Bath    | float | Basement full bathrooms                                                                        |
| Bsmt Qual         | int   | Basement quality - Evaluates the height of the basement                                        |
| BsmtFin SF 1      | float | Type 1 finished square feet                                                                    |
| BsmtFin Type 1    | int   | Rating of basement finished area                                                               |
| Exter Qual        | int   | Rates the overall material and finish of the house                                             |
| Fireplace Qu      | int   | Fireplace quality                                                                              |
| Full Bath         | int   | Full bathrooms above grade                                                                     |
| Garage Area       | float | Size of garage in square feet                                                                  |
| Garage Finish     | int   | Interior finish of the garage                                                                  |
| Garage Qual       | int   | Garage quality                                                                                 |
| Gr Liv Area       | int   | Above grade (ground) living area square feet                                                   |
| Heating QC        | int   | Heating quality and condition                                                                  |
| Kitchen Qual      | int   | Kitchen quality                                                                                |
| Lot Area          | int   | Lot size in square feet                                                                        |
| Mas Vnr Area      | float | Masonry veneer area in square feet                                                             |
| Overall Qual      | int   | Overall quality - Rates the overall material and finish of the house                           |
| TotRms AbvGrd     | int   | Total rooms above grade (does not include bathrooms)                                           |
| Total Bsmt SF     | float | Total square feet of basement area                                                             |
| Wood Deck SF      | int   | Wood deck area in square feet                                                                  |
| ctrl_air_Y        | int   | Central air conditioning: Yes                                                                  |
| ext2nd_VinylSd    | int   | Exterior covering on house (if more than one material) - Vinyl                                 |
| gar_type_BuiltIn  | int   | Built-in garage type                                                                           |
| land_countour_HLS | int   | Land contour: Hillside - Significant slope from side to side                                   |
| neigh_NoRidge     | int   | Northridge neighborhood                                                                        |
| neigh_NridgHt     | int   | Northridge Heights neighborhood                                                                |
| neigh_StoneBr     | int   | Stone Brook neighborhood                                                                       |
| remod_age         | int   | Age of house since remodelling at time of sale.  Same as property age if no remodelling done.  |
| rf_style_Hip      | int   | Type of roof: Hip                                                                              |
| zoning_RM         | int   | Indicates Residential Medium Density zoning classification of the sale                         |

Full data dictionary for the original Ames dataset [here](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).

## Conclusions and Recommendations

### Model comparison

Ridge regression by far has the best test score yet at <mark>88.82%</mark>. With 31 features now, it is now more ideal and easy to explain to relevant stakeholders. Ideally we would always want to have a model that is complex enough to fit all the points but still having enough simplicity to explain your model.

Additionally, the Ridge Regression model does not look to be overfitted as they perform better on the test score.

### Top 5 features from final model

The top feature that highly influences the price at a coefficient of 48313.86 is a property located at Stone Brooks neighbourhood. It is no wonder the best predictor as this neighbourhood is very convenient and is the closest to Iowa State University, the largest university in Iowa state. [[1]](https://en.wikipedia.org/wiki/Iowa_State_University) It is also very close to downtown and is just about a 10 minute drive away. The other two neighbourhoods, Northridge Heights and Northridge are situated close together and is slightly further away to then University but is equidistant to downtown as compared to Stone Brook neighbourhood.
Moreover all three neighbourhoods are very close to elementary, middle and high schools and have amenities really close by. [[2]](https://www.google.com/maps/dir/304+Main+Street,+Ames,+IA/Northridge+Lane,+Ames,+IA/@42.0286767,-93.6589652,14.28z/data=!4m14!4m13!1m5!1m1!1s0x87ee7079a7344bb5:0xda5a2e61aea06f0d!2m2!1d-93.614092!2d42.024838!1m5!1m1!1s0x87ee70c37ac346ef:0x5c6a8eb7cb2ce524!2m2!1d-93.6467454!2d42.0478309!3e0?hl=en-US)

However, it is interesting to note that the land contour that is hilly is valued more than the other land contour features. It is perhaps has a good privacy rating among home dwellers in Ames.

At number five, Overall Quality of the property takes the spot and is no suprise that it is one of the top predictors in property prices, though the coefficient is much lower than being in the top three neighbourhoods.


| Feature       | Coefficient  | Model |
|---------------|--------------|-------|
| neigh_StoneBr | 48313.86    | Ridge Regression |
| neigh_NridgHt | 35155.90    | Ridge Regression|
| neigh_NoRidge | 33220.50    | Ridge Regression |
| land_countour_HLS | 15046.79| Ridge Regression |
| Overall Qual | 11766.23    | Ridge Regression |

Therefore, we can conclude that having a property in those top three neighbourhoods is way more important in highly influencing property prices than Overall Quality.

It is important to note that the above conclusions are only based on the Ames housing dataset. More granular analysis is not possible as the data provided are actual sale prices of houses. In order to complement the above findings, more granular data such as buyer data and coordinates of home sales would be beneficial to delve deep into analysis such as buyer behaviour or neighbourhood studies. This could enable home owners or property developers to better target buyers, or to even educate buyers on the kind of houses they should look out for.

With the right data, it can potentially be an exciting area to look into.
