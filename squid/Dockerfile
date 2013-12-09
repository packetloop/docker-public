FROM  ubuntu:12.04

RUN   echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list.d/ubuntuarchive.list
RUN   apt-get -y update

RUN   apt-get install -qy libreadline6 libreadline6-dev squid

ADD   ./squid.conf /etc/squid3/squid.conf

VOLUME	["/var/log/squid3"]

ENTRYPOINT ["/usr/sbin/squid3"]
CMD	   ["-N","-d","1"]

# sudo docker build -t <username>/squid squid/
# sudo docker push <username>/squid
# sudo docker run -d -p 3128:3128 <username>/squid
