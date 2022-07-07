---
layout: container
name:  "quay.io/biocontainers/kraken2"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/quay.io/biocontainers/kraken2/container.yaml"
updated_at: "2022-07-07 17:20:41.129806"
container_url: "https://quay.io/repository/biocontainers/kraken2"
aliases:
 - "kraken2"

 - "kraken2-build"

 - "kraken2-inspect"

versions:
 - "2.1.1--pl5262h7d875b9_1"
 - "2.1.2--pl5262h7d875b9_0"
 - "2.1.2--pl5321h9f5acd7_2"
description: "A taxonomic classification system using exact k-mer matches to achieve high accuracy and fast classification speeds."
---

This module is a singularity container wrapper for quay.io/biocontainers/kraken2.
A taxonomic classification system using exact k-mer matches to achieve high accuracy and fast classification speeds.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install quay.io/biocontainers/kraken2
```

Or a specific version:

```bash
$ shpc install quay.io/biocontainers/kraken2:2.1.1--pl5262h7d875b9_1
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load quay.io/biocontainers/kraken2/2.1.1--pl5262h7d875b9_1
$ module help quay.io/biocontainers/kraken2/2.1.1--pl5262h7d875b9_1
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### kraken2-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### kraken2-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### kraken2-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### kraken2-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### kraken2-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### kraken2-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### kraken2
       
```bash
$ singularity exec <container> /usr/local/bin/kraken2
$ podman run --it --rm --entrypoint /usr/local/bin/kraken2   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/local/bin/kraken2   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### kraken2-build
       
```bash
$ singularity exec <container> /usr/local/bin/kraken2-build
$ podman run --it --rm --entrypoint /usr/local/bin/kraken2-build   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/local/bin/kraken2-build   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### kraken2-inspect
       
```bash
$ singularity exec <container> /usr/local/bin/kraken2-inspect
$ podman run --it --rm --entrypoint /usr/local/bin/kraken2-inspect   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/local/bin/kraken2-inspect   -v ${PWD} -w ${PWD} <container> -c " $@"
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