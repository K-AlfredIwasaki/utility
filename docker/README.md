
Check available docker images

```
$ docker image ls
```

Build an docker image

DO NOT FORGET `.`

```
$ docker build -t image_name .
```

Run the image

```
$ docker run -it image_name
```

Check what image is running

```
docker ps
```

Remove the image

```
docker rmi -f image_id
```
