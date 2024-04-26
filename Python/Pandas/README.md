# Pandas

### Creating a DataFrame

From Python dictionary: ```DataFrame(data)``` (Python dictionaries are not arrays of objects)

From CSV: ```read_csv('data.csv')```

From JSON: ```read_json('data.json')```


## Summarizing

```info()``` to display the structure (columns...)

```head()``` to print the first 5 rows

```tail()``` to print the last 5 rows

Returns an array of unique values in a columns
```
df['column_name'].unique()
df['column_name'].nunique()   # Just the number of unique values
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
