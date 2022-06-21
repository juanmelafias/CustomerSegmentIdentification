# CustomerSegmentIdentification

This repo contains a Jupyter Notebook displaying a Customer Segment Identification project. 

## Context

A german mailing company wanted to know which population segments where more likely to use their services so they could advertise themselves more effectively.

## Solution

Starting from two databases, one regarding German general population and the other containing just customer population, the goal was to find which population segments were overrepresented in the costumer database with respect to their actual weight in the German population.

### Data Loading and Preprocessing

Before getting hands on machine learning techniques, some preprocessing on our data was applied to ensure the quality of it. Rows and columns containing excessive missing values were dropped first in both sets, and then both datasets were compared to ensure there weren't outliers.

For categorical data, variables were re-encoded into dummy variables. Variables containing multiple sorts of information were also decoded and brought into new different variables.

### Feature Transformation

First, a feature scaling was applied to ensure that Principal Components were not affected by different dimensionalities in the data. Also, missing values were replaced using the most common method row-by-row.
AFter that, variables were projected onto the principal components space, and out of the 80 remaining components, the first 35 were chosen, which amounted for 90% of the explained variance. A close analysis of the first principal componenents was carried out to find out which variables had a greater weight on them.
Then, a K-means cluster was applied to obtain the groups of population

### Comparing general data to customer data

After performing all treatments to both datasets, the percentage of points belonging to each cluster centroid is computed. Those with a higher relative percentage in the customer data will be the target group
.

