################## BASE IMAGE ######################

FROM biocontainers/biocontainers:latest

##############

USER root


RUN apt-get update && \
	apt-get install -y wget lsb-release apt-transport-https && \
	export PLATFORM=$(lsb_release -cs) && \
	wget -O- https://mirror.oxfordnanoportal.com/apt/ont-repo.pub | apt-key add - && \
	echo "deb http://mirror.oxfordnanoportal.com/apt ${PLATFORM}-stable non-free" | tee /etc/apt/sources.list.d/nanoporetech.sources.list && \
	apt-get update

	
RUN mkdir -p /installations
WORKDIR /installations
RUN wget https://mirror.oxfordnanoportal.com/software/analysis/ont-guppy-cpu_4.2.2_linux64.tar.gz
RUN tar -zxf ./ont-guppy-cpu_4.2.2_linux64.tar.gz
ENV PATH="/installations/ont-guppy-cpu/bin/:${PATH}"



USER biodocker

WORKDIR /data/

CMD ["guppy_basecaller"]
