# Pandas / Jupyter Notebook

### General

- Common
```
df.head(), df.tail(), df.summary(), df.describe(), df.shape
```

- Reload functions when they are called
```
%load_ext autoreload
%autoreload 2
```

- Generate a frequncy table
```
df['sub_category'].value_counts()
```
- Specify column width to show in notebook
```
pd.options.display.max_colwidth = 150
```
- Shuffle df rows
```
from sklearn.utils import shuffle
data = shuffle(data, random_state=777)
```

### Merge, join, concatenate

- Join dfs vertically
```
df_combined = pd.concat([df_football, df_basketball, df_baseball])
```

### Indexing
- Indexing --- in vs. not in
- in
```
df[df.a.isin(df.b)]
```
- not in
```
df[~df.a.isin(df.b)]
```

  - not in (a bit complex)
```
df.loc[~df['sub_category'].isin(['OTHERS', 'FOOTBALL','BASKETBALL', 'BASEBALL']),:]
```

### NA
- fillna all columns
```
df.fillna(0, inplace=True)
```


