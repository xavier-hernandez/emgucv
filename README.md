I wanted to create a docker image for some image comparison using .net standard and Emgu.CV in linux but couldn't get it to work out of the box. I kept getting this error...

```
The type initializer for 'Emgu.CV.CvInvoke' threw an exception. ---> System.DllNotFoundException: Unable to load shared library 'cvextern' or one of its dependencies. 
```

Finally found this dockerfile https://github.com/emgucv/docker/blob/master/bazel-android/Dockerfile but changed it for what I needed it for however I also built the image for the original.

Project I'm using it for: https://github.com/xavier-hernandez/tiktok_detection

Docker images: https://hub.docker.com/r/xavierh/emgucv

# emgucv
https://github.com/emgucv

## emgucv-8.0
Some information about the docker image emgucv Dockerfile-8.0
- ubuntu:22.04
- updated to dotnet 8.0
- fixed a bug in original Dockerfile
- removed android functionality

## emgucv-8.0-original
Docker image based off of https://github.com/emgucv/docker/blob/master/bazel-android/Dockerfile
- ubuntu:22.04
- updated to dotnet 8.0
- fixed a bug in their Dockerfile
- android implementation
