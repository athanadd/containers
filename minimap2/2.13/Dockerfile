################## BASE IMAGE ######################

FROM biocontainers/biocontainers:latest

##############

USER root

ENV minimap_url https://github.com/lh3/minimap2/releases/download/v2.13/minimap2-2.13_x64-linux.tar.bz2

RUN mkdir -p /installations
WORKDIR /installations
RUN curl -L ${minimap_url} | tar -jxvf -
ENV PATH="/installations/minimap2-2.13_x64-linux/:${PATH}"

USER biodocker

WORKDIR /data/
