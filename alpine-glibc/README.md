# Alpine with GLIBC 2.28 embedded

An Alpine Linux image with BASH+GLIBC and only 30 MB in size. 
The full list of installable packages and contents may be found on https://pkgs.alpinelinux.org/packages

## DockerHub: 
https://cloud.docker.com/u/afuscella/repository/docker/afuscella/glibc

## Available package manager in container

* apk

## Installed packages

Package         | Version   | Description                                  | Size (after its installation)
:-------------- |:---------:|:---------------------------------------------|------------------------------:
gnupg           | 2.2.15    | GNU Privacy Guard 2 - a PGP replacement tool | ~4.37MB
ca-certificates | 20190108  | Common CA certificates PEM files             | ~720KB
bash            | 5.5.0     | The GNU Bourne Again shell                   | ~1.05MB
glibc           | 2.28      | C compiler library compatible with jdk/jre 8 | ~22MB

## Docker Tags
* alpine:glibc
