# Building image

## Run inside a Docker Container

```
docker build -t 'sheng-fedora-builder' . 
docker run --privileged -v "$(pwd)"/images:/build/images -v "/dev:/dev" sheng-fedora-builder
```

### Building Notes

- ```qemu-user-static``` is also needed if building the image on a ```non-aarch64``` system  