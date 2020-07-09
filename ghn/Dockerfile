FROM node:11

RUN npm update -y -g npm
RUN apt-get update
RUN apt-get install -y vim avahi-daemon libavahi-compat-libdnssd-dev locales
RUN locale-gen ja_JP.UTF-8
RUN echo "export LANG=ja_JP.UTF-8" >> ~/.bashrc

RUN sed -i.bak '/rlimit-nproc=3/d' /etc/avahi/avahi-daemon.conf
RUN git clone https://github.com/sikkimtemi/google-home-voicetext.git
WORKDIR google-home-voicetext
RUN npm install
