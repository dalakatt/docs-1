<!--

********************************************************************************

WARNING:

    DO NOT EDIT "neo4j/README.md"

    IT IS AUTO-GENERATED

    (from the other files in "neo4j/" combined with a set of templates)

********************************************************************************

-->

**Note:** this is the "per-architecture" repository for the `arm64v8` builds of [the `neo4j` official image](https://hub.docker.com/_/neo4j) -- for more information, see ["Architectures other than amd64?" in the official images documentation](https://github.com/docker-library/official-images#architectures-other-than-amd64) and ["An image's source changed in Git, now what?" in the official images FAQ](https://github.com/docker-library/faq#an-images-source-changed-in-git-now-what).

# Quick reference

-	**Maintained by**:  
	[Neo4j](https://github.com/neo4j/docker-neo4j)

-	**Where to get help**:  
	[Neo4j Community Forums](https://community.neo4j.com)

# Supported tags and respective `Dockerfile` links

-	[`4.4.4`, `4.4.4-community`, `4.4`, `4.4-community`, `community`, `latest`](https://github.com/neo4j/docker-neo4j-publish/blob/0b2c95bcf4e2d9c26366890922dfd85d315cb96a/4.4.4/community/Dockerfile)
-	[`4.4.4-enterprise`, `4.4-enterprise`, `enterprise`](https://github.com/neo4j/docker-neo4j-publish/blob/0b2c95bcf4e2d9c26366890922dfd85d315cb96a/4.4.4/enterprise/Dockerfile)
-	[`4.4.3`, `4.4.3-community`](https://github.com/neo4j/docker-neo4j-publish/blob/be7e16fe413f2aa6b5091fc8f6c75787c5894621/4.4.3/community/Dockerfile)
-	[`4.4.3-enterprise`](https://github.com/neo4j/docker-neo4j-publish/blob/be7e16fe413f2aa6b5091fc8f6c75787c5894621/4.4.3/enterprise/Dockerfile)
-	[`4.4.2`, `4.4.2-community`](https://github.com/neo4j/docker-neo4j-publish/blob/f767f9315f828292eb4fc97a7ab48c6243cf60c6/4.4.2/community/Dockerfile)
-	[`4.4.2-enterprise`](https://github.com/neo4j/docker-neo4j-publish/blob/f767f9315f828292eb4fc97a7ab48c6243cf60c6/4.4.2/enterprise/Dockerfile)
-	[`4.4.1`, `4.4.1-community`](https://github.com/neo4j/docker-neo4j-publish/blob/69cfe56e78fd54d3e638f6eed923c8474d2654ef/4.4.1/community/Dockerfile)
-	[`4.4.1-enterprise`](https://github.com/neo4j/docker-neo4j-publish/blob/69cfe56e78fd54d3e638f6eed923c8474d2654ef/4.4.1/enterprise/Dockerfile)
-	[`4.4.0`, `4.4.0-community`](https://github.com/neo4j/docker-neo4j-publish/blob/c3cd89287e0295cbac5ef85de7210ac879934243/4.4.0/community/Dockerfile)
-	[`4.4.0-enterprise`](https://github.com/neo4j/docker-neo4j-publish/blob/c3cd89287e0295cbac5ef85de7210ac879934243/4.4.0/enterprise/Dockerfile)

[![arm64v8/neo4j build status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/multiarch/job/arm64v8/job/neo4j.svg?label=arm64v8/neo4j%20%20build%20job)](https://doi-janky.infosiftr.net/job/multiarch/job/arm64v8/job/neo4j/)

# Quick reference (cont.)

-	**Where to file issues**:  
	[https://github.com/neo4j/docker-neo4j/issues](https://github.com/neo4j/docker-neo4j/issues)

-	**Supported architectures**: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/neo4j/), [`arm64v8`](https://hub.docker.com/r/arm64v8/neo4j/)

-	**Published image artifact details**:  
	[repo-info repo's `repos/neo4j/` directory](https://github.com/docker-library/repo-info/blob/master/repos/neo4j) ([history](https://github.com/docker-library/repo-info/commits/master/repos/neo4j))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images repo's `library/neo4j` label](https://github.com/docker-library/official-images/issues?q=label%3Alibrary%2Fneo4j)  
	[official-images repo's `library/neo4j` file](https://github.com/docker-library/official-images/blob/master/library/neo4j) ([history](https://github.com/docker-library/official-images/commits/master/library/neo4j))

-	**Source of this description**:  
	[docs repo's `neo4j/` directory](https://github.com/docker-library/docs/tree/master/neo4j) ([history](https://github.com/docker-library/docs/commits/master/neo4j))

# What is Neo4j?

Neo4j is the world's leading graph database, with native graph storage and processing. You can learn more [here](http://neo4j.com/developer).

![logo](https://raw.githubusercontent.com/docker-library/docs/56823e63d5b6dd7ddbb9d5d3c4a8947778055d8e/neo4j/logo.png)

# How to use this image

You can start a Neo4j container like this:

```console
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$HOME/neo4j/data:/data \
    arm64v8/neo4j
```

which allows you to access neo4j through your browser at [http://localhost:7474](http://localhost:7474).

This binds two ports (`7474` and `7687`) for HTTP and Bolt access to the Neo4j API. A volume is bound to `/data` to allow the database to be persisted outside the container.

By default, this requires you to login with `neo4j/neo4j` and change the password. You can, for development purposes, disable authentication by passing `--env=NEO4J_AUTH=none` to docker run.

# Documentation

For more examples and complete documentation please go to our manual [here](http://neo4j.com/docs/operations-manual/current/deployment/single-instance/docker/).

# License

View [licensing information](https://neo4j.com/licensing) for the software contained in this image.

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

Some additional license information which was able to be auto-detected might be found in [the `repo-info` repository's `neo4j/` directory](https://github.com/docker-library/repo-info/tree/master/repos/neo4j).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
