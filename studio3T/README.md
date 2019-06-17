Assume we have built this image named as `studio-3t`

* `brew install socat`
* `brew cask install xquartz`
* `socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"`
* `docker run -e DISPLAY=docker.for.mac.host.internal:0 -i -t -d --name s3t --net=host studio-3t /usr/local/studio3t/Studio-3T`
