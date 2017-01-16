[![Docker Hub Automated Build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/zheeeng/keystonejs/)

## Usage

1. Generate/Copy Keystonejs project(exclude the node_modules folder in the project root) and cd into the root directory.
2. Edit your `.env` file
3. Run the keystonejs container:

         docker run -p 80:3000 -it -d -name keystonejs -v "$PWD":/usr/src/app zheeeng/keystonejs

    or optionally link MongoDB container:

         docker run -p 80:3000 -it -d --link your-mongo:mongo --name keystonejs -v "$PWD":/usr/src/app zheeeng/keystonejs

## Note

For Keystonjs only support Node LTS version. Here we use the Node 6.9.4.

For fixing `Cannot find module '../build/Release/bson'] code` bug in:

1. Node v6.9.4
2. NPM 3.10.10
2. MongoDB v3.4.0

We temporary appliy a coping file patch.

