FROM biocontainers/biocontainers:latest

USER root

RUN mkdir -p /installations

WORKDIR /installations

RUN git clone --recursive https://github.com/jts/nanopolish.git
WORKDIR /installations/nanopolish
RUN make

ENV PATH="/installations/nanopolish/:${PATH}"

WORKDIR /data/

CMD ["nanopolish"]
