FROM ubuntu:20.04

# Install riscv gnu toolchain
ENV PATH="${PATH}:/opt/riscv/bin"
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y git autoconf automake autotools-dev curl libmpc-dev libmpfr-dev \
   libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev \
   && git clone https://github.com/riscv-collab/riscv-gnu-toolchain.git \
   && cd riscv-gnu-toolchain \
   && ./configure --prefix=/opt/riscv && make \
   && cd .. && rm -rf riscv-gnu-toolchain
