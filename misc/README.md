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

###  docker install


follow until step 3
- https://pewpewthespells.com/blog/setup_docker_on_mac.html

then encounter the error
```
Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?
```

then refer this stackoverflow post
https://stackoverflow.com/questions/44084846/cannot-connect-to-the-docker-daemon-on-macos

```
brew cask install docker
```

Then launch the Docker app. Click next. It will ask for privileged access. Confirm. A whale icon should appear in the top bar. Click it and wait for "Docker is running" to appear.

```
docker ps
```

### docker command
https://medium.com/@deepakshakya/beginners-guide-to-use-docker-build-run-push-and-pull-4a132c094d75

show the list of docker containers which are running
```
docker ps
```
show the list of all docker containers 
```
docker ps -l
```

run the hello-world container 
```
docker run hello-world
```
exit the container
```
exit
```
### sed

- sed 's/\t/","/g;s/^/"/;s/$/"/;s/\n//g'
  - s/\t/","/g 
  - s/^/"/
  - s/$/"/
  - s/\n//g
 - sed 's/\t/,,,",,,/g;s/\n//g'
 
- g --- apply the replacement to all matches to the regexp










