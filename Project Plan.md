# Business case:

Sam Samson and Sons is a real estate developer looking to adopt a data driven approach to choosing which properties to acquire, remodel, and bring back to market. In particular they want a model to answer the following questions:

1. Which upgrades will yield the highest return?
   - Examples:
     - what is the value of adding a bathroom?
     - what is the value of moving up one or more categories in the quality ranking?
2. Are certain upgrades more valuable in certain areas? If so which factors determine best value remodeling projects?

# Workflow: OSEMN

## Question: Which upgrades yield the highest return?

 	1. **Obtain:** Data was provided by client
 	2. **Scrub:** Clean data
     * For each column:
       * x find and deal with missing values
       * x fix datatypes
         * Track continuous and categorical variables
       * x convert only necessary items to categorical (questioinable cols will be tested later)
         * Don't convert anything to categorical until after the baseline model is created.
	3. **Explore**
    * Answer questions from first section:
      * x Does floors include basement?
    * x Infer values (like finished basement sqft?)
    * x Look for correlations and multicoliniarity
      * Track removed variables
    * Create baseline model (here because iterations will happen in the model phase)
    * Explore distributions (don't modify them yet)
    * Normlaize data (here because exploration is easier with real numbers)
	4. **Model**
    * Create baseline model (how many features??)
    * Remove insignifgant features
    * Test questionable features as categorical or continuous
      * Should grade be reduced to 3 categories
    * Look for possible interactions (zipcode and bathroom?)
	5. **iNterpret**
    * Build visuals to describe findings
    * Create presentation

