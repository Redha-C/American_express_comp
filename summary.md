Results : 
    - The target is not related to the categorical features, there is not a single value which pops out for default payments 
    - mean of P_2, P_3 is higher for target = 0 but lower for P_4, R_2, R_3 and R_4 => make the features Mohamed Chahhou talked about for those features for sure 

    Next steps : 
        - Find train/test split : done 
        - Perform a bit of EDA : 
            - Look at the categorical features, their unique values to try to understand what they are and think about their missing value imputation : done 
            - Look at the number of features for each type of column (use Kaggle platform) : done 
            - Look at the numerical features and try to understand them :
                - checkout mean vs median to think about missing value imputation for P and R columns: done 
                - checkout mean vs median for D, S and columns (check the difference straight)
        - Impute missing values :
            - check if some rows are totally empty => delete them 
        - Check the data selection step from the pipeline 
        - Find the best CV method 