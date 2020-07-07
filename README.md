# containers

Docker containers are an excelent way to isolate running applications and make your research or work more reproducible.
I usually try to use containers in my in silico biological research and bioinformatics analysis. One excelent repository, namely biocontainers, maintains a great collection of tools applicable to biological analyses.

### Dockerfiles
The Dockerfiles are special text files that can be used with Docker to build standalone images of selected applications.
In this repo I store Dockerfiles of applications usually relevant to biology, that I could not find anywhere else, so I had to build.
*I do not own any of the applications used in these containers.*
Feel free to use and modify the provided Dockerfiles to build your own images.

### Pre-built containers
Pre-built containers can be downloaded from my DockerHub. Links are available in each container seperately.

To build the containers use the command:
$ docker build - < Dockerfile

For more information you can refer to the official [Docker website](https://docs.docker.com/engine/reference/commandline/build)
