#
#Build the image
#docker build -t libre-office
#Use below command to run the libreoffice
#docker run --rm --net=host --env="DISPLAY" -v $HOME/.Xauthority:/root/.Xauthority:rw -v $HOME/libreOfficeSavedFile:/home libre-office
#save your all work to home folder in container to get copy to local directory libreOfficeSavedFile 
#
#
#


FROM ubuntu:14.04

RUN apt-get update \
    && apt-get -y install curl \
    && curl -O https://mirrors.estointernet.in/tdf/libreoffice/stable/6.1.4/deb/x86_64/LibreOffice_6.1.4_Linux_x86-64_deb.tar.gz \
    && apt-get update 
    
RUN apt-get -y remove curl

RUN tar -xzf LibreOffice_6.1.4_Linux_x86-64_deb.tar.gz && rm LibreOffice_6.1.4_Linux_x86-64_deb.tar.gz

RUN apt-get -y install libglu1-mesa \
    && apt-get -y install libxinerama1 


RUN cd /LibreOffice_6.1.4.2_Linux_x86-64_deb/DEBS && dpkg -i *.deb 

RUN rm -r tmp
RUN rm -rf /var/lib/apt/lists/*

CMD ["/usr/bin/libreoffice6.1"]
