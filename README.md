Fedora CI
=========

There are images called `fedora` that are Fedora images with
Qt dependencies, used to build Liri projects with Travis CI.

And there are images for Jenkins.
The [docker-workflow-plugin](https://github.com/jenkinsci/docker-workflow-plugin)
forces Docker containers to run as unprivileged user, using the UID and GID
of the Jenkins user.
This image is based on our Fedora-based container for Travis CI builds,
but adds the `jenkins` user and it's ready for Jenkins.  We also provide
a sudo configuration that allows to run `sudo` without password.

Make the image with:

```sh
sudo make build
```

Push to the Docker hub:

```sh
sudo make push
```
