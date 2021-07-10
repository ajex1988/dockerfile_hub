FROM ubuntu:18.04
LABEL maintainer="ajex1988@gmail.com"
RUN DEBIAN_FRONTEND="noninteractive" apt update && apt install -y python3.6 python3-pip git-all
RUN pip install opencv-python
RUN pip3 install torch==1.9.0+cu111 torchvision==0.10.0+cu111 torchaudio==0.9.0 -f https://download.pytorch.org/whl/torch_stable.html
RUN mkdir /workspace/projects
RUN cd /workspace/projects && git clone --recurse-submodules https://github.com/dusty-nv/pytorch-ssd.git