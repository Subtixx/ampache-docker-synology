# ampache-docker

Docker container for Ampache, a web based audio/video streaming application and file manager allowing you to access your music & videos from anywhere, using almost any internet enabled device.

![travis status](https://travis-ci.org/arielelkin/ampache-docker.svg?branch=master)

## Usage

The recommended way to run ampache-docker is by using the current github packages.

To run the current Ampache master (stable) branch
```bash
docker run --name=ampache -d -v /path/to/your/music:/media:ro -p 80:80 docker.pkg.github.com/ampache/ampache-docker/ampache:latest
```
To run the current Ampache develop branch
```bash
docker run --name=ampache -d -v /path/to/your/music:/media:ro -p 80:80 docker.pkg.github.com/ampache/ampache-docker/ampache:develop
```

To run using the docker hub image (NOT RECOMMENDED! It's years out of date.)
```bash
docker run --name=ampache -d -v /path/to/your/music:/media:ro -p 80:80 ampache/ampache
```

## Installation
- MySQL Administrative Username: root # leave alone
- MySQL Administrative Password:      # (blank) leave alone
- Check "Create Database User"
- Ampache Database Username: ampache
- Ampache Database User Password: ampache # or whatever you want, but remember it on the next page
- next page fill out MySQL Username / Password
- Click the "Write" buttons from BOTTOM to TOP
- Do this because it is the last one that needs the username and password and they get blanked out on every click

## Thanks to
- @ericfrederich for his original work
- @velocity303 and @goldy for the other ampache-docker inspiration
