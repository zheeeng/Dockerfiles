FROM ubuntu:latest

LABEL maintainer "Zheeeng <hi@zheeeng.me>"

RUN apt-get update && apt-get install -y \
    curl libswt-gtk-3-java

RUN curl https://download.studio3t.com/studio-3t/linux/2019.3.0/studio-3t-linux-x64.tar.gz --output studio-3t-linux-x64.tar.gz && tar -xvzf studio-3t-linux-x64.tar.gz && yes "" | ./studio-3t-linux-x64.sh && rm studio-3t-linux-x64.*

CMD /usr/local/studio3t/Studio-3T
