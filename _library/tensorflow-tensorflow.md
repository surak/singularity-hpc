---
layout: container
name:  "tensorflow/tensorflow"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/tensorflow/tensorflow/container.yaml"
updated_at: "2022-08-01 18:14:13.977081"
container_url: "https://hub.docker.com/r/tensorflow/tensorflow"
aliases:
 - "python"

versions:
 - "2.5.0-custom-op-gpu-ubuntu16"
 - "2.5.0rc0-gpu-jupyter"
 - "2.6.0"
 - "2.6.0rc0-gpu-jupyter"
 - "2.7.0"
 - "2.7.0rc0"
 - "2.8.0"
 - "2.8.0rc0"
 - "latest-gpu"
 - "2.7.1-gpu"
 - "2.7.1"
 - "2.6.1"
 - "2.5.1"
 - "2.9.0rc1"
 - "2.9.1"
 - "2.8.2"
 - "2.7.3"
description: "An end-to-end open source platform for machine learning."
---

This module is a singularity container wrapper for tensorflow/tensorflow.
An end-to-end open source platform for machine learning.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install tensorflow/tensorflow
```

Or a specific version:

```bash
$ shpc install tensorflow/tensorflow:2.5.0-custom-op-gpu-ubuntu16
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load tensorflow/tensorflow/2.5.0-custom-op-gpu-ubuntu16
$ module help tensorflow/tensorflow/2.5.0-custom-op-gpu-ubuntu16
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### tensorflow-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### tensorflow-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### tensorflow-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### tensorflow-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### tensorflow-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### tensorflow-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### python
       
```bash
$ singularity exec <container> /usr/local/bin/python
$ podman run --it --rm --entrypoint /usr/local/bin/python   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/local/bin/python   -v ${PWD} -w ${PWD} <container> -c " $@"
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