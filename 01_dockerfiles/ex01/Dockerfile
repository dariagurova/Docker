FROM debian

RUN apt-get -y update && apt-get -y upgrade &&\
apt-get -y install wget bzip2 && \
wget http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 && \
tar xfv teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2

CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]