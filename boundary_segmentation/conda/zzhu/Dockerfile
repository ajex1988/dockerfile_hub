FROM nvidia/cuda:9.2-devel-ubuntu18.04
LABEL maintainer="ajex1988@gmail.com"
RUN apt update && apt install -y curl git vim ninja-build libgl1-mesa-glx libglib2.0-0 python-pip
RUN pip install ipython imagecorruptions Polygon3 tqdm mmcv==0.4.3
RUN curl https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh -o ~/anaconda.sh
RUN  /bin/bash ~/anaconda.sh -b -p /opt/conda && rm ~/anaconda.sh
SHELL ["/bin/bash", "-c", "source /opt/conda/bin/activate"]
SHELL ["conda", "init"]
#RUN source /opt/conda/bin/activate && conda init
#RUN conda create --name open-mmlab python=3.7 -y && conda activate open-mmlab && conda install cython -y
#RUN conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=9.2 -c pytorch -y