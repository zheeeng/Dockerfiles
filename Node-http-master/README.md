[![Docker Hub Automated Build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/zheeeng/node-http-master/)

## Http-master Official Doc

<https://github.com/virtkick/http-master>

## Usage Example

1. Create your configuration file, for example: 

        // file: http-master.config.json
        {
          "ports": {
            "80": {
              "router": {
                "blog.zheeeng.me" : "keystonejs:3000",
                "forum.zheeeng.me" : "nodebb:4567"
              }
            }
          }
        }

2. Run the http-master container, for example:

         docker run -p 80:80 -it -d --name http-master -l keystonejs -l nodebb -v "$PWD"/http-master.config.json:/usr/configs/http-master.config.json zheeeng/node-http-master http-master --config /usr/configs/http-master.json --watch
