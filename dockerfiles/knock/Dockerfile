#knock environment
#Knock is a subdomain Scanner details https://github.com/guelfoweb/knock
 
FROM ubuntu:15.04
MAINTAINER nahidupa@gmail.com
RUN apt-get update \
 && apt-get install -y git python wget
RUN wget https://bootstrap.pypa.io/ez_setup.py -O - | python
WORKDIR "/opt"
RUN mkdir gitclone
WORKDIR "/opt/gitclone"
RUN git clone https://github.com/guelfoweb/knock.git
WORKDIR "/opt/gitclone/knock"
RUN chmod +x setup.py
RUN ./setup.py install

# Clean up
RUN apt-get autoremove
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && rm -r /opt/gitclone
