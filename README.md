A tool helps to build a deep learning docker environment quickly.

## Build

```
make <TARGET> <ARG>=1 ...
```

**TARGET** are supported following,

| Target | Image | Description |
|--------|-------|-------------|
| build-tf-gpu | ubuntu:18.04-tf-gpu | Build a docker image with tensorflow and cuda environment. |

**ARG** are supported following,

| Argument | Description |
|----------|-------------|
| DOWNLOAD_CUDA | Download cuda when build image |
| AUTO_VIM | Configure [autoVim](https://github.com/yechenglin-dev/autoVim) in image |

## Usage

Run a image,

```
docker run -d -v /lib/modules:/libmodules --privileged --name -p 999:22 tf <IMAGE>
```

Login container via ssh,

```
ssh -p 999 tf@localhost
```

> Password is **testpass**.
