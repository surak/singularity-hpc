---
layout: container
name:  "ghcr.io/autamus/lmod"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/ghcr.io/autamus/lmod/container.yaml"
updated_at: "2022-07-07 17:19:36.975160"
container_url: "https://github.com/orgs/autamus/packages/container/package/lmod"
aliases:
 - "module"

versions:
 - "8.3"
 - "8.5.6"
 - "8.5.9"
 - "8.5.12"
 - "8.5.13"
 - "8.5.27"
 - "8.6.3"
 - "latest"
description: "The Persistence of Vision Ray Tracer, most commonly acronymed as POV-Ray, is a cross-platform ray-tracing program that generates images from a text-based scene description."
---

This module is a singularity container wrapper for ghcr.io/autamus/lmod.
The Persistence of Vision Ray Tracer, most commonly acronymed as POV-Ray, is a cross-platform ray-tracing program that generates images from a text-based scene description.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install ghcr.io/autamus/lmod
```

Or a specific version:

```bash
$ shpc install ghcr.io/autamus/lmod:8.3
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load ghcr.io/autamus/lmod/8.3
$ module help ghcr.io/autamus/lmod/8.3
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### lmod-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### lmod-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### lmod-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### lmod-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### lmod-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### lmod-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### module
       
```bash
$ singularity exec <container> . /opt/view/lmod/8.3/init/profile && module
$ podman run --it --rm --entrypoint .   -v ${PWD} -w ${PWD} <container> -c "/opt/view/lmod/8.3/init/profile && module $@"
$ docker run --it --rm --entrypoint .   -v ${PWD} -w ${PWD} <container> -c "/opt/view/lmod/8.3/init/profile && module $@"
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