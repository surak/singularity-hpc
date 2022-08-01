---
layout: container
name:  "quay.io/biocontainers/cutadapt"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/quay.io/biocontainers/cutadapt/container.yaml"
updated_at: "2022-08-01 15:28:31.143467"
container_url: "https://quay.io/repository/biocontainers/cutadapt"
aliases:
 - "cutadapt"

versions:
 - "3.4--py36h4c5857e_0"
 - "3.4--py38h4a8c8d9_1"
 - "3.5--py39h38f01e4_0"
 - "3.7--py38hbff2b2d_0"
description: "Trim adapters from high-throughput sequencing reads"
---

This module is a singularity container wrapper for quay.io/biocontainers/cutadapt.
Trim adapters from high-throughput sequencing reads
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install quay.io/biocontainers/cutadapt
```

Or a specific version:

```bash
$ shpc install quay.io/biocontainers/cutadapt:3.4--py36h4c5857e_0
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load quay.io/biocontainers/cutadapt/3.4--py36h4c5857e_0
$ module help quay.io/biocontainers/cutadapt/3.4--py36h4c5857e_0
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### cutadapt-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### cutadapt-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### cutadapt-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### cutadapt-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### cutadapt-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### cutadapt-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### cutadapt
       
```bash
$ singularity exec <container> /usr/local/bin/cutadapt
$ podman run --it --rm --entrypoint /usr/local/bin/cutadapt   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/local/bin/cutadapt   -v ${PWD} -w ${PWD} <container> -c " $@"
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