# Precious Metal Price Analysis

***Can we reliably predict the price of silver? And is it about to go way up?***

## Motivation

Someone approached me not long ago and said something interesting that got me thinking a bit. They said something to the effect of: "you have to buy this thing, the value is going to skyrocket soon, and I wouldn't want you to miss out. I've been watching this for a long time, and I'm telling you, it's going to be big." The appeal was compelling, especially to the innate psychological tendencies that make us human (the kids call this 'FOMO' or 'Fear Of Missing Out'). But something felt off, and I ultimately brushed off the opportunity, said my thanks, and moved on without much further thought.

The 'golden opportunity' (pun intended) presented to me was in precious metal investments, particularly silver. The logic was that the price of silver was tied to the price of gold, and silver was significantly undervalued relative to gold at that time. During the winter holidays of 2022, when this conversation happened, the theory was that the gold-silver price ratio was 7:1. That balance made the theoretical price point for silver in the neighborhood of $270/ounce, a price that outpaced the going spot by over 10x. This failed common sense check led me to walk away, but I also never thoroughly investigated the claim until now.

To get started, here's a plot of the relationship of interest:

<img src="https://github.com/andrewkroening/precious-metal-price-analysis/blob/e6f8269f63b195ff08e7d78dffb8108de9b73d7c/40_imagery/gold_silver_price_over_time.png" alt="Gold-Silver Prices" width="1000"/>

## Data

For this exploration, I'll be using monthly average prices for various commodities that I've collected from the International Monetary Fund (IMF); the data can be found [at this link](https://www.imf.org/en/Research/commodity-prices). The IMF maintains historical prices on a wide variety of commodities and indices from around the world, which it aggregates as a monthly average price in the form I collected.

## [Exploratory Data Analysis](https://github.com/andrewkroening/precious-metal-price-analysis/blob/e6f8269f63b195ff08e7d78dffb8108de9b73d7c/20_code/exploratory_analysis.ipynb)

The Exploratory data analysis portion of this project sought to downselect the ImF dataset from ~94 variables to the handful that are most closely associated and likely to have the best predictive value for silver. I examined several facets of the data to include plotting prices over time and correlations to silver. In the end, I arrived at three groups of predictors:

#### Group 1: Copper, Platinum, and Aluminum

<img src="https://github.com/andrewkroening/precious-metal-price-analysis/blob/872a838913f82ff9cb4c4c4ee33b1684ed0dc2dc/40_imagery/copper_comp_chart.png" alt="Copper-Silver Prices" width="400"/><img src="https://github.com/andrewkroening/precious-metal-price-analysis/blob/872a838913f82ff9cb4c4c4ee33b1684ed0dc2dc/40_imagery/aluminum_comp_chart.png" alt="Aluminum-Silver Prices" width="400"/><img src="https://github.com/andrewkroening/precious-metal-price-analysis/blob/872a838913f82ff9cb4c4c4ee33b1684ed0dc2dc/40_imagery/platinum_comp_chart.png" alt="Platinum-Silver Prices" width="400"/>

#### Group 2: Gold

<img src="https://github.com/andrewkroening/precious-metal-price-analysis/blob/872a838913f82ff9cb4c4c4ee33b1684ed0dc2dc/40_imagery/gold_comp_chart.png" alt="Gold-Silver Prices" width="400"/>

#### Group 3: Tin and Lead

<img src="https://github.com/andrewkroening/precious-metal-price-analysis/blob/872a838913f82ff9cb4c4c4ee33b1684ed0dc2dc/40_imagery/tin_comp_chart.png" alt="Tin-Silver Prices" width="400"/><img src="https://github.com/andrewkroening/precious-metal-price-analysis/blob/872a838913f82ff9cb4c4c4ee33b1684ed0dc2dc/40_imagery/lead_comp_chart.png" alt="Lead-Silver Prices" width="400"/>
