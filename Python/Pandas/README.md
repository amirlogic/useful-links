# Pandas

## Creating a DataFrame

From Python dictionary: ```DataFrame(data)``` (Python dictionaries are not arrays of objects)

From CSV: ```read_csv('data.csv')```

From JSON: ```read_json('data.json')```


## Index

The index of a DataFrame is a series of labels that identify each row. The labels can be integers, strings, or any other hashable type.

Can be accessed or modified using: ```df.index()```


## Columns


### Get values

```df.columns.values```


### Rename

```df.rename(columns={'col0':'new col0','col1':'new col1','col2':'new col2'}, inplace=True)```


### Merge

```df['merged'] = pd.concat([df['col1'], df['col2']])```


## Summarizing

```info()``` to display the structure (columns...)

```head()``` to print the first 5 rows

```tail()``` to print the last 5 rows

Returns an array of unique values in a columns
```python
df['column_name'].unique()
df['column_name'].nunique()   # Just the number of unique values
```

Count Rows inside a Group
```python
df['column_name'].value_counts()
```


## Cleaning

Deleting duplicates:
```python
df.drop_duplicates()
```

```df.dropna(subset=['column_name'])``` Remove empty cells

Filling NaN values using the previous and next values:
```python
df[column].interpolate()
```

## Modifying

### Replacing values:

```python
df['column_name'].str.replace('search','replaceby')
```

### Deleting values

Columns:

```python
newdf = df.drop("age", axis='columns')
```

Rows:

```python
newdf = df.drop(99, axis='index')
```

### Casting

To numeric:

```python
pd.to_numeric(df['col_name'], errors='coerce')
```

Advantage: Can handle non-numeric values

astype:

```python
df.astype({'col_name': 'float'},errors='ignore').dtypes
```

Returns unchanged series (or error) if non-numeric values are present


## Links

Exercises https://github.com/guipsamora/pandas_exercises

Introduction to Pandas Data Analysis https://www.youtube.com/watch?v=DkjCaAMBGWM

Exploratory Data Analysis https://www.youtube.com/watch?v=xi0vhXFPegw


## Datasets to explore
