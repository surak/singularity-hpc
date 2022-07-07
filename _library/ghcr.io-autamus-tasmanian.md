---
layout: container
name:  "ghcr.io/autamus/tasmanian"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/ghcr.io/autamus/tasmanian/container.yaml"
updated_at: "2022-07-07 17:21:39.111781"
container_url: "https://github.com/orgs/autamus/packages/container/package/tasmanian"
aliases:
 - "tasgrid"

versions:
 - "7.5"
 - "7.7"
 - "latest"
description: "The Toolkit for Adaptive Stochastic Modeling and Non-Intrusive ApproximatioN is a robust library for high dimensional integration and interpolation as well as parameter calibration.  https://tasmanian.ornl.gov"
---

This module is a singularity container wrapper for ghcr.io/autamus/tasmanian.
The Toolkit for Adaptive Stochastic Modeling and Non-Intrusive ApproximatioN is a robust library for high dimensional integration and interpolation as well as parameter calibration.  https://tasmanian.ornl.gov
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install ghcr.io/autamus/tasmanian
```

Or a specific version:

```bash
$ shpc install ghcr.io/autamus/tasmanian:7.5
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load ghcr.io/autamus/tasmanian/7.5
$ module help ghcr.io/autamus/tasmanian/7.5
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### tasmanian-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### tasmanian-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### tasmanian-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### tasmanian-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### tasmanian-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### tasmanian-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### tasgrid
       
```bash
$ singularity exec <container> /opt/view/bin/tasgrid
$ podman run --it --rm --entrypoint /opt/view/bin/tasgrid   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /opt/view/bin/tasgrid   -v ${PWD} -w ${PWD} <container> -c " $@"
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