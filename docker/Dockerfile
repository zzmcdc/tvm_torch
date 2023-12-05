FROM nvcr.io/nvidia/pytorch:20.01-py3
ENV TZ=Asia/Shanghai 
ENV DEBIAN_FRONTEND=noninteractive 

RUN apt-get update && apt-get install -y sudo clang llvm  \
    python3-dev python3-pip  libopenblas-dev cmake ninja-build ccache lldb apt-transport-https\
    ca-certificates wget unzip make  automake build-essential g++ git psmisc tzdata  pkg-config  \
    libopenblas-dev libboost-all-dev libjpeg-dev  locales \
    && locale-gen zh_CN zh_CN.GB18030 zh_CN.GBK zh_CN.UTF-8 en_US.UTF-8 \
    && update-locale && cp -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo 'Asia/Shanghai' >/etc/timezone \
    && apt-get clean && rm -rf /var/lib/apt/lists/* 
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8
