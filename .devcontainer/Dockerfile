FROM mcr.microsoft.com/devcontainers/cpp:1-debian-12

ARG REINSTALL_CMAKE_VERSION_FROM_SOURCE="none"

COPY ./reinstall-cmake.sh /tmp/
RUN if [ "${REINSTALL_CMAKE_VERSION_FROM_SOURCE}" != "none" ]; then \
        chmod +x /tmp/reinstall-cmake.sh && /tmp/reinstall-cmake.sh ${REINSTALL_CMAKE_VERSION_FROM_SOURCE}; \
    fi \
    && rm -f /tmp/reinstall-cmake.sh

RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y libboost-dev
RUN git clone https://github.com/atcoder/ac-library.git -b v1.5.1