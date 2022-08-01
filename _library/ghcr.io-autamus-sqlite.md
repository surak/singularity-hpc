---
layout: container
name:  "ghcr.io/autamus/sqlite"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/ghcr.io/autamus/sqlite/container.yaml"
updated_at: "2022-08-01 15:08:31.702918"
container_url: "https://github.com/orgs/autamus/packages/container/package/sqlite"
aliases:
 - "sqlite3"

versions:
 - "3.35.4"
 - "3.35.5"
 - "3.36.0"
 - "3.37.1"
 - "latest"
 - "3.37.2"
 - "3.38.3"
description: "SQLite is a relational database management system contained in a C library. "
---

This module is a singularity container wrapper for ghcr.io/autamus/sqlite.
SQLite is a relational database management system contained in a C library. 
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install ghcr.io/autamus/sqlite
```

Or a specific version:

```bash
$ shpc install ghcr.io/autamus/sqlite:3.35.4
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load ghcr.io/autamus/sqlite/3.35.4
$ module help ghcr.io/autamus/sqlite/3.35.4
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### sqlite-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### sqlite-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### sqlite-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### sqlite-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### sqlite-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### sqlite-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### sqlite3
       
```bash
$ singularity exec <container> /opt/view/bin/sqlite3
$ podman run --it --rm --entrypoint /opt/view/bin/sqlite3   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /opt/view/bin/sqlite3   -v ${PWD} -w ${PWD} <container> -c " $@"
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