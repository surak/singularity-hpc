---
layout: container
name:  "ghcr.io/autamus/picard"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/ghcr.io/autamus/picard/container.yaml"
updated_at: "2022-07-07 17:20:24.630939"
container_url: "https://github.com/orgs/autamus/packages/container/package/picard"
aliases:
 - "picard"

 - "picard.jar"

versions:
 - "2.25.2"
 - "2.25.3"
 - "2.25.4"
 - "2.25.5"
 - "2.25.6"
 - "2.26.0"
 - "2.26.4"
 - "2.26.5"
 - "latest"
 - "2.25.7"
description: "A set of command line tools (in Java) for manipulating high-throughput sequencing (HTS) data and formats such as SAM/BAM/CRAM and VCF."
---

This module is a singularity container wrapper for ghcr.io/autamus/picard.
A set of command line tools (in Java) for manipulating high-throughput sequencing (HTS) data and formats such as SAM/BAM/CRAM and VCF.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install ghcr.io/autamus/picard
```

Or a specific version:

```bash
$ shpc install ghcr.io/autamus/picard:2.25.2
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load ghcr.io/autamus/picard/2.25.2
$ module help ghcr.io/autamus/picard/2.25.2
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### picard-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### picard-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### picard-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### picard-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### picard-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### picard-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### picard
       
```bash
$ singularity exec <container> /opt/view/bin/picard
$ podman run --it --rm --entrypoint /opt/view/bin/picard   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /opt/view/bin/picard   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### picard.jar
       
```bash
$ singularity exec <container> /opt/view/bin/java -jar /opt/view/bin/picard.jar
$ podman run --it --rm --entrypoint /opt/view/bin/java   -v ${PWD} -w ${PWD} <container> -c "-jar /opt/view/bin/picard.jar $@"
$ docker run --it --rm --entrypoint /opt/view/bin/java   -v ${PWD} -w ${PWD} <container> -c "-jar /opt/view/bin/picard.jar $@"
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