docker-sge
==========

Dockerfile to build a container with SGE installed.

To build type:

```
git clone git@github.com:stevekm/docker-sge.git
cd docker-sge
docker build -t stevekm/docker-sge .
```

To pull from the Docker Hub type:

```
docker pull gawbul/docker-sge
```

To run the image in a container type:

```
docker run -it --rm gawbul/docker-sge login -f sgeadmin

docker run -it --rm stevekm/docker-sge login -f sgeadmin
```

**You need the `login -f sgeadmin` as root isn't allowed to submit jobs**

To submit a job run:

```
echo "echo Running test from $HOSTNAME" | qsub
```
