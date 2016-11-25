FROM node:6.9.1

RUN apt-get update && apt-get install -y \
  git \
  wget \
  vim \
  net-tools \
  > /dev/null

#  python-dev \
#  python-setuptools \
#  python-pip \
#  python-numpy \  
#  python-scipy \
#  python-tables \
#  python-numexpr \
#  ipython \


RUN npm install gulp  -g && npm install webpack -g 

RUN cd ~ && git clone https://github.com/jakebian/hera.git
RUN cd ~/hera/server && npm install && gulp
RUN cd ~/hera/client && npm install


# Create app directory
#RUN mkdir -p /usr/src/app
#WORKDIR /usr/src/app

EXPOSE 3000
EXPOSE 4000
