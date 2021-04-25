ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/cpp:0-${VARIANT}

RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y libboost1.71-dev
RUN git clone https://github.com/atcoder/ac-library.git -b v1.3
