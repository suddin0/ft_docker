FROM debian:latest
ADD http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 .
RUN apt-get update && apt-get install bzip2
ADD script1 .
RUN ["/bin/bash", "/script1"]
ENTRYPOINT ["/bin/bash", "run_st3_server.sh"]

#TO BUILD  THE COMMAND : docker build -t ts3_server .
#TO LAUNCH THE COMMAND : docker run --rm  -p 9987:9987/udp -p 30033:30033 -p 10011:10011 -p 41144:41144 --pid=host ts3_server
