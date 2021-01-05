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
       * find and deal with missing values
       * fix datatypes
       * convert only necessary items to categorical (questioinable cols will be tested later)
       * normalize definitivly continuous variables
     * Infer values (like finished basement sqft?)
	3. **Explore**
    * Look for correlations and multicoliniarity
    * Explore distributions
    * Normlaize data
	4. **Model**
    * Create baseline model (how many features??)
    * Remove insignifgant features
    * Test questionable features as categorical or continuous
    * Look for possible interactions (zipcode and bathroom?)
	5. **iNterpret**
    * Build visuals to describe findings
    * Create presentation

