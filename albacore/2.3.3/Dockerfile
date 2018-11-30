################## BASE IMAGE ######################

FROM biocontainers/biocontainers:latest

##############

USER root


RUN apt-get update && \
	apt-get install -y wget apt-transport-https libboost-all-dev python3-setuptools && \
	wget -O- https://mirror.oxfordnanoportal.com/apt/ont-repo.pub | apt-key add - && \
	echo "deb http://mirror.oxfordnanoportal.com/apt trusty-stable non-free" | tee /etc/apt/sources.list.d/nanoporetech.sources.list && \
	apt-get update

RUN mkdir -p /installations && \
	cd /installations && \
	wget https://mirror.oxfordnanoportal.com/software/analysis/python3-ont-albacore_2.3.3-1~xenial_amd64.deb
RUN dpkg -i /installations/python3-ont-albacore_2.3.3-1~xenial_amd64.deb || :
RUN apt-get install -fy

USER biodocker

WORKDIR /data/
