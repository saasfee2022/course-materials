# Saas-Fee 2022 hand-on session materials

This repository will contain materials for Saas-Fee 2022 hands-on sessions.

For now, feel free to [start a session](https://renkulab.io/projects/saasfee2022/course-materials/sessions/new?autostart=1), find the *Welcome.ipynb* notebook, and experiment with it:

<img src="renku-saas-nb-tutorial.png"/>

## Using RenkuLab

Although it is possible to start a session for quick investigation without a `renku` account, it is advisable that your create one.
This way, you will be able to see list of your session (https://renkulab.io/sessions/) and even commit your work in your own fork of the course materials repository.

Please visit  https://renkulab.io and create an account. You can also login with GitHub, ORCID, etc.

To start new session:

https://renkulab.io/projects/saasfee2022/course-materials/sessions/new?autostart=1



## Offline container image (slow or unavailable network)

### Preparation before the course

You will recieve a container image on an USB stick, including all of the needed data and software for the course.

As previously requested, every participant should have docker installed.
In addition, to avoid any dependency on the network, we ask everyone to download this small image in advance

```bash
$ docker pull odahub/saasfee22-offline-bootstrap:latest
```

Also, please download this small test image and put it in the current directory (mouse right click and "save link as" or equivalent; take care that the file is saved with the original name - some browsers add an extra extension to it, like ".txt"):

https://www.isdc.unige.ch/~savchenk/saasfee22-welcome-and-test.sif

To test that you are able to use the image, run:

```bash
$ docker run -it -v $PWD/saasfee22-welcome-and-test.sif:/image.sif -it --rm --privileged odahub/saasfee22-offline-bootstrap:latest
```
