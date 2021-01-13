# Good Enough

This is an expiriment in creating a **quick** `good enough` model to see how well a simple workflow can work.  This is based on my struggles with ordering events to create the `best` model for the data set.  In reality the best model may only be marginally better than a very good `good enough` model, so if `good enough` takes a few hours and `best` takes a week `good enough` could provide more business value.

## Work Flow

### Get Started

	1. Imports
	2. Import Data
	3. Drop Duplicates
	4. Create usable (not necessarily the final) datatypes
	  	1. Find missing values
	  	2. 
	5. Create a baseline model.

### Data Understanding

1. I have alread done this so I will skip it for this test

### Prepare tools

	1. Function for Crosfold testing
	2. Simple Function that only returns R2 & RMSEs.
	3. Create a Dict for tracking model progress.

### Iterate the model

#### 	Look at each variable individually

 1. Create a new DataFrame for each variable

 2. Try to improve R2 and RMSE without overfitting.
    	1. Remove Outliers
        	2. Change to Categorical if necessary
        	3. If it are correlated? Can they be used in another way?
           	1. Transform?
           	2. Interraction?

	3. Transform if necessary for linearity assumption

	4. Train a model and store results for each iteration

	5. Repeat for all independent variables.

#### Deal with any remaining correlation and multicoliniarity.

1. use vif score to handle multicoliniarity of varibles of interest
   1. Bathrooms
   2. sqft_living_diff_sqft_living15
   3. condition
   4. Bedrooms
2. Try
   1. center
   2. scale
3. Verify correlations

#### Check model assumptions

1. See if problems can be fixed
   1. Transform dependent variable?

