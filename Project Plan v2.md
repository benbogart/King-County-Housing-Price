# Business case:

Sam Samson and Sons is a real estate developer looking to adopt a data driven approach to choosing which properties to acquire, remodel, and bring back to market. In particular they want a model to answer the following questions:

1. Which upgrades will yield the highest return?
   - Examples:
     - what is the value of adding a bathroom?
     - what is the value of moving up one or more categories in the quality ranking?
   - Are certain upgrades more valuable in certain areas? If so which factors determine best value remodeling projects?
2. Determine the profit potential of a remodel on a listing.  i.e. how much more can a remodel sell for after taking certain steps like adding a bathroom.

# Workflow: CRISP-DM

## Question: Which upgrades yield the highest return?

 	1. **Obtain:** Data was provided by client
 	2. **Data Understanding**
     * Look for duplicates
     * Questions
       * x Does floors include basement?
       * Relationship of Lat, Long, Zip to price?
     * x Look for correlations and multicoliniarity
       * xTrack removed variables
 	3. **Data Preparation** Clean data
     * For each column:
       * x find and deal with missing values
       * x fix datatypes
         * Track continuous and categorical variables
       * x convert only necessary items to categorical (questioinable cols will be tested later)
         * Don't convert anything to categorical until after the baseline model is created.
	4. **Baseline Modeling**
    * Create baseline model
      * Use stepwise feature selection (QUESTION: Does multicolinierity affect p value??)
      * Validate LR assumptions [Need Help]
        * Linearity
        * x Normality - https://learning.flatironschool.com/courses/1409/assignments/48030?module_item_id=92096
          * x QQ 
          * x Jarque-Bera Test
        * Homosedasticity - https://learning.flatironschool.com/courses/1409/assignments/48030?module_item_id=92096
          * 
      * Check MSE (REVIEW THIS IN COURSE MATERIAL)
	5. **Data Preparation - Remodel**
    * Check value of making questionable features categorical
      * NOTE: more features will raise R<sup>2</sup>, check R<sup>2</sup><sub>adj</sub>  
    * Incorporate geographic data
      * bin zipcodes
      * create quadrents
    * Explore effects of standardization of each variable independently
    * Explore the effects of normalization of each variable independently
    * Explore the effects of log transformation on each variable independently
    * Look for interactions with unused data
      * zipcode and bathroom or sqft
      * Lat & long
	6. **Evaluate/Interpret**
    * Build visuals to describe findings
    * Create presentation

