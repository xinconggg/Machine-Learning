# Machine Learning Checklist

## Main Steps:
1. Frame the problem and look at the big picture.
2. Get the data.
3. Explore the data to gain insights.
4. Prepare the data to better expose underlying patterns to Machine Learning algorithms.
5. Explore many different models and short-list the best ones.
6. Fine-tune the models and combine them into a great solution.
7. Present the solution.
8. Launch, monitor, and maintain the system.

---

## Step 1: Frame the Problem and Look at the Big Picture
1. Define the objective in business terms.
2. Determine how the solution will be used.
3. Identify current solutions or workarounds, if any.
4. Frame the problem appropriately (e.g., supervised/unsupervised, online/offline learning).
5. Define performance metrics.
6. Ensure performance metrics align with the business objective.
7. Establish the minimum performance required to meet the objective.
8. Identify comparable problems to leverage existing experience or tools.
9. Assess the availability of human expertise.
10. Consider how a human would solve the problem manually.
11. List any assumptions made.
12. Verify the assumptions, where possible.

---

## Step 2: Get the Data
*Automate data retrieval to ensure fresh data can be accessed easily.*

1. List the required data and its volume.
2. Document the data sources.
3. Estimate storage requirements.
4. Verify legal obligations and obtain necessary authorizations.
5. Secure access permissions.
6. Set up a workspace with adequate storage.
7. Retrieve the data.
8. Convert the data into a manipulatable format without altering its integrity.
9. Protect sensitive information (e.g., through anonymization).
10. Assess the data size and type (e.g., time series, geographical).
11. Sample a test set and set it aside to avoid data snooping.

---

## Step 3: Explore the Data
*Seek insights from domain experts during this phase.*

1. Create a copy of the data for exploration (downsample if necessary).
2. Use a Jupyter notebook to document the exploration process.
3. Examine each attribute:
   - Name
   - Type (categorical, numeric, text, etc.)
   - Percentage of missing values
   - Noisiness and noise type (outliers, rounding errors, etc.)
   - Potential usefulness for the task
   - Distribution type (Gaussian, uniform, etc.)
4. Identify target attributes for supervised learning tasks.
5. Visualize the data.
6. Analyze correlations between attributes.
7. Consider manual solutions to the problem.
8. Identify promising data transformations.
9. Determine if additional data is needed.
10. Document findings.

---

## Step 4: Prepare the Data
*Maintain the integrity of the original dataset by working with copies.*

1. **Data Cleaning:**
   - Address outliers.
   - Handle missing values (fill with mean/median or drop).
2. **Feature Selection (optional):**
   - Remove attributes with no utility for the task.
3. **Feature Engineering:**
   - Discretize continuous features.
   - Decompose features (e.g., categorical values, timestamps).
   - Apply transformations (e.g., log, square root).
   - Aggregate features to create new attributes.
4. **Feature Scaling:**
   - Standardize or normalize features.

---

## Step 5: Short-List Promising Models
*Consider sampling smaller training sets for efficiency when working with large datasets.*

1. Train diverse models quickly (e.g., linear models, SVMs, Random Forests).
2. Compare model performance using N-fold cross-validation.
3. Identify the most significant variables for each model.
4. Analyze the types of errors made by each model.
5. Perform additional feature selection and engineering.
6. Iterate through the above steps as needed.
7. Short-list the top three to five models, ensuring they handle errors differently.

---

## Step 6: Fine-Tune the System
*Use as much data as possible during this phase.*

1. Optimize hyperparameters using cross-validation.
   - Treat data transformation choices as hyperparameters.
   - Prefer random search over grid search when exploring hyperparameters.
   - Consider Bayesian optimization for lengthy training processes.
2. Utilize ensemble methods to combine models.
3. Measure the final model’s performance on the test set to estimate generalization error.
   - Avoid modifying the model post-test to prevent overfitting.

---

## Step 7: Present the Solution
1. Document all work done throughout the project.
2. Create a presentation that highlights the overarching goal and solution.
3. Explain how the solution achieves the business objective.
4. Share insights gained, including what worked and what didn’t.
5. List assumptions made and limitations of the system.
6. Use visual aids to effectively communicate key findings.

---

## Step 8: Launch, Monitor, and Maintain the System
1. Prepare the solution for production by integrating it with live data inputs.
2. Develop monitoring tools to track system performance over time.
   - Set alerts for performance drops.
   - Monitor for gradual degradation.
3. Regularly retrain models with fresh data to ensure continued relevance.
   - Automate the retraining process where feasible.
4. Monitor input data quality to detect and address anomalies (e.g., faulty sensors, outdated data sources).

