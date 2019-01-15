#
#Build the image
#docker build -t libre-office
#Use below command to run the libreoffice
#docker run --rm --net=host --env="DISPLAY" -v $HOME/.Xauthority:/root/.Xauthority:rw -v $HOME/libreOfficeSavedFile:/home libre-office
#
#save your all work to home folder in container to get copy to local directory libreOfficeSavedFile 
#
#
#

FROM ubuntu:14.04

Run apt-get update \
    && apt-get -y install software-properties-common \
    && add-apt-repository ppa:libreoffice/ppa \
    && apt-get update \
    && apt-get -y install libreoffice 

Run apt-get -y remove software-properties-common
#removed apt list
RUN rm -rf /var/lib/apt/lists/*

CMD ["/usr/bin/libreoffice"]






