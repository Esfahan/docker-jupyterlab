# docker-jupyterlab
Docker container for jupyterlab

## Installation
Pull the image.

```
$ sudo docker pull jupyter/datascience-notebook
```

build

```
$ sudo docker build -t jupyterlab:latest ./
```

## Generate a password
Generate a password for jupyterlab.

```
$ /bin/generate-password

Enter password:
Verify password:
# Use this with running jupyterlab
sha1:xxxxxxxxxxxxxxxxxxxxxxxx
```

## Run
Run jupyterlab.

```
$ ./bin/jupyterlab
Hashed password: {Enter the hased password `sha1:xxxxxxxxxxxxxxxxxxxxxxxx`}
```

- `code` directory is mounted on container.
  - `-v $(pwd)/code:/code`
- Fowarding port from 8888 to 8888
  - `-p 8888:8888`

## Browse
http://localhost:8888
