# Week 5 Cheat Sheet

## common imports 
# Models
from sklearn.ensemble import RandomForestClassifier, RandomForestRegressor, GradientBoostingClassifier
from sklearn.linear_model import LogisticRegression, LinearRegression, Ridge, Lasso
from sklearn.tree import DecisionTreeClassifier

# Preprocessing
from sklearn.preprocessing import StandardScaler, MinMaxScaler, RobustScaler
from sklearn.preprocessing import OrdinalEncoder, OneHotEncoder, LabelEncoder
from sklearn.impute import SimpleImputer, KNNImputer

# Pipeline
from sklearn.pipeline import Pipeline
from sklearn.compose import ColumnTransformer

# Model Selection
from sklearn.model_selection import train_test_split, cross_val_score, KFold, StratifiedKFold
from sklearn.model_selection import GridSearchCV, RandomizedSearchCV

# Metrics
from sklearn.metrics import accuracy_score, f1_score, precision_score, recall_score
from sklearn.metrics import mean_squared_error, r2_score, confusion_matrix

# Feature Selection
from sklearn.feature_selection import SelectKBest, f_classif, RFE
from sklearn.inspection import permutation_importance






##  Day 4
# Pipeline
# Chains multiple steps (imputer → scaler → model) into one object.
# fit() on pipeline = fit_transform() each step in order, fit() on final estimator.
# Prevents data leakage — transformers only see training data during fit.
# One fit() call, one predict() call. Works with GridSearchCV automatically.

# ColumnTransformer
# Applies different transformations to different column subsets simultaneously.
# Numerical columns → imputer + scaler
# Categorical columns → imputer + OneHotEncoder
# Combines outputs into one feature matrix automatically.

# BaseEstimator + TransformerMixin
# BaseEstimator → gives get_params() and set_params() free
# TransformerMixin → gives fit_transform() free
# You only write fit() and transform()
# Makes custom transformer plug directly into Pipeline and GridSearchCV