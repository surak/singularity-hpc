---
layout: container
name:  "ghcr.io/autamus/protobuf"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/ghcr.io/autamus/protobuf/container.yaml"
updated_at: "2022-08-01 18:13:21.768983"
container_url: "https://github.com/orgs/autamus/packages/container/package/protobuf"
aliases:
 - "protoc"

 - "protoc-3.15.8.0"

versions:
 - "3.15.8"
 - "3.16.0"
 - "3.17.0"
 - "3.17.2"
 - "3.17.3"
 - "3.19.1"
 - "latest"
 - "3.19.0"
 - "3.18.1"
description: "Protocol Buffers is a method of serializing structured data. It is useful in developing programs to communicate with each other over a network or for storing data."
---

This module is a singularity container wrapper for ghcr.io/autamus/protobuf.
Protocol Buffers is a method of serializing structured data. It is useful in developing programs to communicate with each other over a network or for storing data.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install ghcr.io/autamus/protobuf
```

Or a specific version:

```bash
$ shpc install ghcr.io/autamus/protobuf:3.15.8
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load ghcr.io/autamus/protobuf/3.15.8
$ module help ghcr.io/autamus/protobuf/3.15.8
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### protobuf-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### protobuf-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### protobuf-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### protobuf-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### protobuf-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### protobuf-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### protoc
       
```bash
$ singularity exec <container> /opt/view/bin/protoc
$ podman run --it --rm --entrypoint /opt/view/bin/protoc   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /opt/view/bin/protoc   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### protoc-3.15.8.0
       
```bash
$ singularity exec <container> /opt/view/bin/protoc-3.15.8.0
$ podman run --it --rm --entrypoint /opt/view/bin/protoc-3.15.8.0   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /opt/view/bin/protoc-3.15.8.0   -v ${PWD} -w ${PWD} <container> -c " $@"
```



In the above, the `<container>` directive will reference an actual container provided
by the module, for the version you have chosen to load. An environment file in the
module folder will also be bound. Note that although a container
might provide custom commands, every container exposes unique exec, shell, run, and
inspect aliases. For anycommands above, you can export:

 - SINGULARITY_OPTS: to define custom options for singularity (e.g., --debug)
 - SINGULARITY_COMMAND_OPTS: to define custom options for the command (e.g., -b)
 - PODMAN_OPTS: to define custom options for podman or docker
 - PODMAN_COMMAND_OPTS: to define custom options for the command

<br>
  
### Install

You can install shpc locally (for yourself or your user base) as follows:

```bash
$ git clone https://github.com/singularityhub/singularity-hpc
$ cd singularity-hpc
$ pip install -e .
```

Have any questions, or want to request a new module or version? [ask for help!](https://github.com/singularityhub/singularity-hpc/issues)