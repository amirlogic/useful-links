# Matplotlib

## Start

```python
import matplotlib.pyplot as plt
```

## Bar

```python
plt.bar(df['BRAND'],df['Q1 2024'])
plt.xlabel('Q1 2024')
plt.ylabel('Sales')
plt.show() 
```


## Customization

```python
plt.xticks(rotation = 90)
```


## Saving plots

```python
plt.savefig(fname)
```

