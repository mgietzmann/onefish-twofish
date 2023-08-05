FROM ubuntu:18.04
MAINTAINER "Marcel Gietzmann-Sanders" "marcelsanders96@gmail.com"

RUN apt-get -y update && \
    apt-get -y upgrade && \
    apt-get -y install build-essential

# add python and libraries
RUN apt-get -y install python3.6 && \
	apt-get -y install python3-pip && \
	pip3 install --upgrade setuptools pip
RUN echo "alias python=python3.6" >> /root/.bashrc

# add jupyter lab
RUN pip install jupyterlab==3.2.9

# add git, vim and curl
RUN apt-get -y install git vim curl

# useful libraries for this project
RUN pip install pandas==1.1.5 \
	plotly==5.15.0 \
	scikit-learn==0.24.2 \
	scipy==1.5.4 \
	tqdm==4.64.1
