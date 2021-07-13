FROM ubuntu:18.04
LABEL maintainer="ajex1988@gmail.com"
ENV TZ=Etc/GMT+6
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ARG DEBIAN_FRONTEND=noninteractive
RUN apt update && apt install -y python3.6 python3-pip python-pip git-all vim \
  libpython-dev \
  cmake \
  libgoogle-glog-dev \
  python-numpy \
  openssh-server \
  unzip \
  gdb

RUN pip install opencv-python==4.2.0.32
RUN pip3 install torch==1.9.0+cu111 torchvision==0.10.0+cu111 torchaudio==0.9.0 -f https://download.pytorch.org/whl/torch_stable.html
RUN mkdir /workspace/projects
RUN cd /workspace/projects && git clone --recurse-submodules https://github.com/dusty-nv/pytorch-ssd.git