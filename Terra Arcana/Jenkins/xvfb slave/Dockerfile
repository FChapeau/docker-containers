FROM jenkinsci/jnlp-slave
MAINTAINER Francois Drouin-Morin
USER root

RUN apt-get update
RUN apt-get install xvfb x11-xkb-utils xfonts-100dpi xfonts-75dpi xfonts-scalable xfonts-cyrillic x11-apps git sudo -y
RUN useradd -m docker && echo "docker:docker" | chpasswd && adduser docker sudo

RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
RUN sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
RUN apt-get update
RUN apt-get install google-chrome-stable -y
