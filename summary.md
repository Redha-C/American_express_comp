Results : 
    - The target is not related to the categorical features, there is not a single value which pops out for default payments 
    - mean of P_2, P_3 is higher for target = 0 but lower for P_4, R_2, R_3 and R_4 => make the features Mohamed Chahhou talked about for those features for sure 
    - Missing values : 
        - train : 31 features have more than 50% of missing values (D_87,D_88,D_108,D_110,D_111,B_39,D_73,B_42,D_134,D_137,D_138,D_135,D_136,R_9,B_29,D_106,D_132,D_49,R_26,D_76,D_66,D_42,D_142,D_53,D_82,D_50,B_17,D_105,D_56,S_9,D_77)
        - test : 31 features have more than 50% of missing values (D_87,D_88,D_108,D_110,D_111,B_39,D_73,B_42,D_134,D_136,D_137,D_138,D_135,R_9,D_76,D_66,D_106,D_132,D_49,D_42,R_26,D_142,B_29,D_82,D_53,D_50,B_17,D_105,D_56, D_77)

    Next steps : 
        - Find train/test split : done 
        - Perform a bit of EDA : 
            - Look at the categorical features, their unique values to try to understand what they are and think about their missing value imputation : done 
            - Look at the number of features for each type of column (use Kaggle platform) : done 
            - Look at the numerical features and try to understand them :
                - checkout mean vs median to think about missing value imputation for P and R columns: done 
                - checkout mean vs median for D, S and columns (check the difference straight) : done
        - Impute missing values :
            - check if some rows are totally empty to delete them, maybe : done 
            - Delete columns with ~ more than 50% of missing values : done 
            - Replace other missing values without concatenating train and test and use kaggle platform to help  
        - Find the best CV method using RF
        - Check noisy features (use tip from Mohamed Chahhou) to remove potential top ranked noisy features
        - Check correlation between non-noisy features and target
        - Check the data selection step from the pipeline 
        - For feature engineering :
            - create the useful features presented by Mohamed Chahhou