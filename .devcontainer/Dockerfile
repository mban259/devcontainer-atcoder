ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/cpp:0-${VARIANT}

RUN git clone https://github.com/atcoder/ac-library.git -b v1.3

RUN wget https://dl.bintray.com/boostorg/release/1.71.0/source/boost_1_71_0.tar.bz2
RUN tar xf boost_1_71_0.tar.bz2
WORKDIR /boost_1_71_0
RUN ./bootstrap.sh --prefix=/opt/boost/gcc
RUN ./b2 install
