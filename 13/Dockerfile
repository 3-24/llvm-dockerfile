FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y wget lsb-release wget software-properties-common gnupg

WORKDIR /root

RUN wget https://apt.llvm.org/llvm.sh && \
    chmod +x llvm.sh && \
    ./llvm.sh 13 all

COPY update-alternatives.sh /root

RUN chmod +x ./update-alternatives.sh && \
    ./update-alternatives.sh 13 1