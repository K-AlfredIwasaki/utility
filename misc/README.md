### boto3
- load a datafame as a csv file to s3
```
from io import BytesIO
import boto3

csv_buffer = BytesIO()
df_combined.to_csv(csv_buffer, sep='|', index=False)
file_name = 'df_sports_additional.csv'
key = 'tmp/data/classification/data_second_layer/' + file_name
bucket = 'smart-newsdev-dmp'
s3_resource = boto3.resource('s3')
s3_resource.Object(bucket, file_name).put(Key=key, Body=csv_buffer.getvalue())
```


