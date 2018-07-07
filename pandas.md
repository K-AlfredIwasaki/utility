
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
### Dropping 

### 




### Managing NA
- fi
- llna all columns
```
df.fillna(0, inplace=True)
```

### S3

import boto3

def upload_to_s3(bucket, folder, file):
    s3 = boto3.resource('s3')
    data = open(file, "rb")
    key = folder + file
    s3.Bucket(bucket).put_object(Key=key, Body=data)

bucket = 'sn-deepnews'
folder = 'DEV/master-consolidated/'
outputfile = 'master-EN-category.csv'

df_merged.to_csv(outputfile, sep='\t', index = False)
upload_to_s3(bucket, folder, outputfile)
!!rm 'master-EN-category.csv'

