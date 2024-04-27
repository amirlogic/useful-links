# Pandas

## Creating a DataFrame

From Python dictionary: ```DataFrame(data)``` (Python dictionaries are not arrays of objects)

From CSV: ```read_csv('data.csv')```

From JSON: ```read_json('data.json')```


## Index

The index of a DataFrame is a series of labels that identify each row. The labels can be integers, strings, or any other hashable type.

Can be accessed or modified using: ```df.index()```


## Summarizing

```info()``` to display the structure (columns...)

```head()``` to print the first 5 rows

```tail()``` to print the last 5 rows

Returns an array of unique values in a columns
```
df['column_name'].unique()
df['column_name'].nunique()   # Just the number of unique values
```

Count Rows inside a Group
```
df['column_name'].value_counts()
```


## Cleaning

Deleting duplicates:
```
df.drop_duplicates()
```

```df.dropna(subset=['column_name'])``` Remove empty cells


## Modifying

Replacing values:
```
df['column_name'].str.replace('search','replaceby')
```


## Filtering



## Links

Exercises https://github.com/guipsamora/pandas_exercises

Introduction to Pandas Data Analysis https://www.youtube.com/watch?v=DkjCaAMBGWM

Exploratory Data Analysis https://www.youtube.com/watch?v=xi0vhXFPegw


## Datasets to explore
