---
layout: container
name:  "ghcr.io/autamus/aria2"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/ghcr.io/autamus/aria2/container.yaml"
updated_at: "2022-08-01 15:27:36.893880"
container_url: "https://github.com/orgs/autamus/packages/container/package/aria2"
aliases:
 - "aria2c"

versions:
 - "1.35.0"
 - "1.36.0"
 - "latest"
description: "aria2 is a lightweight multi-protocol & multi-source command-line download utility."
---

This module is a singularity container wrapper for ghcr.io/autamus/aria2.
aria2 is a lightweight multi-protocol & multi-source command-line download utility.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install ghcr.io/autamus/aria2
```

Or a specific version:

```bash
$ shpc install ghcr.io/autamus/aria2:1.35.0
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load ghcr.io/autamus/aria2/1.35.0
$ module help ghcr.io/autamus/aria2/1.35.0
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### aria2-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### aria2-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### aria2-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### aria2-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### aria2-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### aria2-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### aria2c
       
```bash
$ singularity exec <container> opt/view/bin/aria2c
$ podman run --it --rm --entrypoint opt/view/bin/aria2c   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint opt/view/bin/aria2c   -v ${PWD} -w ${PWD} <container> -c " $@"
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