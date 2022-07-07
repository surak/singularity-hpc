---
layout: container
name:  "nvcr.io/nvidia/rapidsai/rapidsai"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/nvcr.io/nvidia/rapidsai/rapidsai/container.yaml"
updated_at: "2022-07-07 17:20:32.500593"
container_url: "https://ngc.nvidia.com/catalog/containers/nvidia:rapidsai:rapidsai/tags"
aliases:
 - "python"

versions:
 - "0.18-cuda11.0-runtime-centos7"
 - "22.02-cuda11.5-runtime-ubuntu20.04"
 - "21.10-cuda11.2-runtime-ubuntu20.04"
 - "21.08-cuda11.2-runtime-ubuntu20.04"
 - "21.06-cuda11.2-runtime-ubuntu20.04"
 - "cuda11.5-runtime-ubuntu20.04"
 - "22.04-cuda11.5-runtime-ubuntu20.04"
description: "The RAPIDS suite of software libraries gives you the freedom to execute end-to-end data science and analytics pipelines entirely on GPUs."
---

This module is a singularity container wrapper for nvcr.io/nvidia/rapidsai/rapidsai.
The RAPIDS suite of software libraries gives you the freedom to execute end-to-end data science and analytics pipelines entirely on GPUs.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install nvcr.io/nvidia/rapidsai/rapidsai
```

Or a specific version:

```bash
$ shpc install nvcr.io/nvidia/rapidsai/rapidsai:0.18-cuda11.0-runtime-centos7
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load nvcr.io/nvidia/rapidsai/rapidsai/0.18-cuda11.0-runtime-centos7
$ module help nvcr.io/nvidia/rapidsai/rapidsai/0.18-cuda11.0-runtime-centos7
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### rapidsai-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### rapidsai-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### rapidsai-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### rapidsai-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### rapidsai-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### rapidsai-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### python
       
```bash
$ singularity exec <container> /opt/conda/bin/python
$ podman run --it --rm --entrypoint /opt/conda/bin/python   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /opt/conda/bin/python   -v ${PWD} -w ${PWD} <container> -c " $@"
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