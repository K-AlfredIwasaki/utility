
### Configure AWS CLI

https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html

### Using the AWS CLI with Amazon ECR

https://docs.aws.amazon.com/AmazonECR/latest/userguide/ECR_AWSCLI.html

Step 1: Authenticate Docker to your Default Registry

1. Run the aws ecr get-login command
```
aws ecr get-login --no-include-email
```
Output:
```
docker login -u AWS -p password https://aws_account_id.dkr.ecr.us-east-1.amazonaws.com
```
2. Copy and paste the docker login command into a terminal to authenticate your Docker CLI

Step 2: Get a Docker Image

Example
```
$ docker pull ubuntu:trusty
```

Step 3: Create a Repository

```
aws ecr create-repository --repository-name ubuntu
```
Step 4: Push an Image to Amazon ECR

To tag and push an image to Amazon ECR

1. List the images you have stored locally to identify the image to tag and push.
```
docker images
```

2. Tag the image to push to your repository.
```
docker tag ubuntu:trusty aws_account_id.dkr.ecr.us-east-1.amazonaws.com/ubuntu:trusty
```

3. Push the image.

```
docker push aws_account_id.dkr.ecr.us-east-1.amazonaws.com/ubuntu:trusty
```

Step 5: Pull an Image from Amazon ECR

After your image has been pushed to your Amazon ECR repository, you can pull it from other locations.
```
docker pull aws_account_id.dkr.ecr.us-east-1.amazonaws.com/ubuntu:trusty
```

Step 6: Delete an Image

```
$ aws ecr batch-delete-image --repository-name ubuntu --image-ids imageTag=trusty
```

Step 7: Delete a Repository


```
$ aws ecr delete-repository --repository-name ubuntu --force
```

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




### sed

- sed 's/\t/","/g;s/^/"/;s/$/"/;s/\n//g'
  - s/\t/","/g 
  - s/^/"/
  - s/$/"/
  - s/\n//g
 - sed 's/\t/,,,",,,/g;s/\n//g'
 
- g --- apply the replacement to all matches to the regexp











