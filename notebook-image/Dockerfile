FROM docker.io/fedora:26

RUN dnf install -y \
python3-pip \
python3-notebook \
python3-ipython \
python3-requests \
python3-numpy \
python3-scipy \
python3-pandas \
python3-matplotlib \
python3-seaborn \
python3-scikit-learn \
python3-scikit-image \
python3-bleach \
python3-markdown \
python3-werkzeug \
python3-wheel \
&& useradd --create-home -s /bin/bash nb

WORKDIR /home/nb
USER nb

RUN pip3 install --user tensorflow keras \
&& mkdir .keras \
&& mkdir .jupyter \
&& mkdir notebooks

COPY keras.json .keras/keras.json
COPY jupyter_notebook_config.py .jupyter/jupyter_notebook_config.py
