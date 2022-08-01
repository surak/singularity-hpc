---
layout: container
name:  "elasticsearch"
maintainer: "@vsoch"
github: "https://github.com/singularityhub/singularity-hpc/blob/main/registry/elasticsearch/container.yaml"
updated_at: "2022-08-01 15:23:11.689400"
container_url: "https://hub.docker.com/_/elasticsearch"
aliases:
 - "elasticsearch"

 - "elasticsearch-certgen"

 - "elasticsearch-certutil"

 - "elasticsearch-cli"

 - "elasticsearch-croneval"

 - "elasticsearch-env"

 - "elasticsearch-env-from-file"

 - "elasticsearch-keystore"

 - "elasticsearch-migrate"

 - "elasticsearch-node"

 - "elasticsearch-plugin"

 - "elasticsearch-saml-metadata"

 - "elasticsearch-setup-passwords"

 - "elasticsearch-shard"

 - "elasticsearch-sql-cli"

 - "elasticsearch-sql-cli-7.12.0.jar"

 - "elasticsearch-syskeygen"

 - "elasticsearch-users"

versions:
 - "7.12.0"
 - "7.12.1"
 - "7.13.1"
 - "7.13.2"
 - "7.13.3"
 - "7.14.0"
 - "7.14.2"
 - "7.16.2"
 - "7.16.3"
 - "8.0.0"
 - "8.1.2"
 - "8.0.1"
 - "7.17.2"
 - "8.1.3"
 - "7.17.3"
 - "8.2.2"
 - "7.17.4"
 - "8.3.1"
 - "8.2.3"
 - "7.17.5"
 - "8.3.3"
description: "Elasticsearch is a powerful open source search and analytics engine that makes data easy to explore."
---

This module is a singularity container wrapper for elasticsearch.
Elasticsearch is a powerful open source search and analytics engine that makes data easy to explore.
After [installing shpc](#install) you will want to install this container module:


```bash
$ shpc install elasticsearch
```

Or a specific version:

```bash
$ shpc install elasticsearch:7.12.0
```

And then you can tell lmod about your modules folder:

```bash
$ module use ./modules
```

And load the module, and ask for help, or similar.

```bash
$ module load elasticsearch/7.12.0
$ module help elasticsearch/7.12.0
```

You can use tab for auto-completion of module names or commands that are provided.

<br>

### Commands

When you install this module, you will be able to load it to make the following commands accessible.
Examples for both Singularity, Podman, and Docker (container technologies supported) are included.

#### elasticsearch-run:

```bash
$ singularity run <container>
$ podman run --rm  -v ${PWD} -w ${PWD} <container>
$ docker run --rm  -v ${PWD} -w ${PWD} <container>
```

#### elasticsearch-shell:

```bash
$ singularity shell -s /bin/sh <container>
$ podman run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
$ docker run --it --rm --entrypoint /bin/sh  -v ${PWD} -w ${PWD} <container>
```

#### elasticsearch-exec:

```bash
$ singularity exec <container> "$@"
$ podman run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
$ docker run --it --rm --entrypoint ""  -v ${PWD} -w ${PWD} <container> "$@"
```

#### elasticsearch-inspect:

Podman and Docker only have one inspect type.

```bash
$ podman inspect <container>
$ docker inspect <container>
```

#### elasticsearch-inspect-runscript:

```bash
$ singularity inspect -r <container>
```

#### elasticsearch-inspect-deffile:

```bash
$ singularity inspect -d <container>
```


#### elasticsearch
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-certgen
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-certgen
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-certgen   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-certgen   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-certutil
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-certutil
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-certutil   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-certutil   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-cli
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-cli
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-cli   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-cli   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-croneval
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-croneval
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-croneval   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-croneval   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-env
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-env
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-env   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-env   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-env-from-file
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-env-from-file
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-env-from-file   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-env-from-file   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-keystore
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-keystore
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-keystore   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-keystore   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-migrate
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-migrate
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-migrate   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-migrate   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-node
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-node
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-node   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-node   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-plugin
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-plugin
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-plugin   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-plugin   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-saml-metadata
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-saml-metadata
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-saml-metadata   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-saml-metadata   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-setup-passwords
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-setup-passwords
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-setup-passwords   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-setup-passwords   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-shard
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-shard
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-shard   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-shard   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-sql-cli
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-sql-cli
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-sql-cli   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-sql-cli   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-sql-cli-7.12.0.jar
       
```bash
$ singularity exec <container> java jar /usr/share/elasticsearch/bin/elasticsearch-sql-cli-7.12.0.jar
$ podman run --it --rm --entrypoint java   -v ${PWD} -w ${PWD} <container> -c "jar /usr/share/elasticsearch/bin/elasticsearch-sql-cli-7.12.0.jar $@"
$ docker run --it --rm --entrypoint java   -v ${PWD} -w ${PWD} <container> -c "jar /usr/share/elasticsearch/bin/elasticsearch-sql-cli-7.12.0.jar $@"
```


#### elasticsearch-syskeygen
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-syskeygen
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-syskeygen   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-syskeygen   -v ${PWD} -w ${PWD} <container> -c " $@"
```


#### elasticsearch-users
       
```bash
$ singularity exec <container> /usr/share/elasticsearch/bin/elasticsearch-users
$ podman run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-users   -v ${PWD} -w ${PWD} <container> -c " $@"
$ docker run --it --rm --entrypoint /usr/share/elasticsearch/bin/elasticsearch-users   -v ${PWD} -w ${PWD} <container> -c " $@"
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