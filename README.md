# Common pandas Functions for Machine Learning

Below is a list of common pandas functions you might use when preparing data for a machine learning project.

---

## 1. Data Import and Inspection

- **`pd.read_csv("file.csv")`**  
  Reads a CSV file into a DataFrame.

- **`df.head()`**  
  Shows the first few rows of the DataFrame.

- **`df.tail()`**  
  Shows the last few rows of the DataFrame.

- **`df.info()`**  
  Gives an overview of data types and non-null counts.

- **`df.describe()`**  
  Returns descriptive statistics for numeric columns.

---

## 2. Handling Missing Values

- **`df.isnull().sum()`**  
  Shows the total count of missing values per column.

- **`df.dropna()`**  
  Drops rows (or columns) with missing values.

- **`df.fillna(value)`**  
  Fills missing values with a given value or method (e.g., `method='ffill'`).

---

## 3. Data Cleaning & Transformation

- **`df.drop_duplicates()`**  
  Removes duplicate rows.

- **`df.rename(columns={"old_name": "new_name"})`**  
  Renames columns.

- **`df['col'].astype(new_dtype)`**  
  Converts a column to a specified data type.

- **`df['col'].apply(function)`**  
  Applies a custom function to each element in a column.

- **`df.loc[row_indexer, col_indexer]`**  
  Selects data by label.

- **`df.iloc[row_indexer, col_indexer]`**  
  Selects data by integer position.

---

## 4. Feature Engineering

- **`df['new_col'] = df['col1'] + df['col2']`**  
  Creates a new feature by combining existing columns.

- **`pd.get_dummies(df['categorical_col'])`**  
  Applies one-hot encoding to a categorical variable.

- **`df['col'].map(mapping_dict)`**  
  Replaces the values of a column using a dictionary map.

---

## 5. Exploratory Data Analysis (EDA)

- **`df['col'].value_counts()`**  
  Counts occurrences of each category in a column.

- **`df.corr()`**  
  Computes pairwise correlation between columns.

- **`df.describe(include='all')`**  
  Gives descriptive stats for numeric and object columns.

---

## 6. Data Grouping & Aggregation

- **`df.groupby('col').mean()`**  
  Groups by a column and calculates the mean for all numeric columns.

- **`df.groupby('col').agg(['count', 'mean', 'max', ...])`**  
  Aggregates multiple metrics.

- **`pd.pivot_table(df, values='val_col', index='row_col', columns='col_col', aggfunc='mean')`**  
  Reshapes data into a pivot table.

---

## 7. Merging & Combining Data

- **`pd.merge(df1, df2, on='key_column', how='inner')`**  
  Merges two DataFrames on a key (inner, left, right, outer).

- **`pd.concat([df1, df2], axis=0 or 1)`**  
  Stacks DataFrames vertically (`axis=0`) or side by side (`axis=1`).

---

## 8. Data Export

- **`df.to_csv("output.csv", index=False)`**  
  Saves the DataFrame to a CSV file.

---

## 9. Integration with Machine Learning

- **`X = df.drop('target', axis=1)`**  
  Splits features from the target column.

- **`y = df['target']`**  
  Sets the target column separately.

- **`train_test_split(X, y, test_size=0.2, random_state=42)`**  
  Splits data into training and testing sets (from scikit-learn).

---

