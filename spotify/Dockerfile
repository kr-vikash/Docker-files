FROM ubuntu:14.04

##Build command
#docker build -t spotify .
##Run command
#docker run --rm --net=host --device /dev/snd --env="DISPLAY"  spotify
#

RUN apt-get update \
    && apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 931FF8E79F0876134EDDBDCCA87FF9DF48BF1C90 \
    && echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list \
    && apt-get update \
    && apt-get --force-yes -y install spotify-client

RUN groupmod -g 92 audio

CMD ["spotify"]
 
