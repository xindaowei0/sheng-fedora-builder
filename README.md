# pipa-fedora-builder

Huge thanks to: [fedora-asahi-builder](https://github.com/leifliddy/asahi-fedora-builder) and [nabu-fedora-build](https://github.com/nik012003/nabu-fedora-builder)

Builds a Fedora image to run on Xiaomi Mi Pad 6

## Fedora Package Install

```dnf install arch-install-scripts bubblewrap systemd-container zip```

### Building Notes

- ```qemu-user-static``` is also needed if building the image on a ```non-aarch64``` system  

## Run inside a Docker Container

```
docker build -t 'pipa-fedora-builder' . 
docker run --privileged -v "$(pwd)"/images:/build/images -v "/dev:/dev" pipa-fedora-builder
```

### User Notes

1. The root password is **fedora**
2. The user password is 147147
