ARG JUPYTER_VERSION
FROM jupyter/datascience-notebook:${JUPYTER_VERSION}

USER root
RUN \
 apt update &&\
 apt install -y \
  libgl1-mesa-glx \
  xvfb
USER jovyan

COPY requirements.in requirements.in
RUN \
  pip install --upgrade \
    pip \
    pip-tools &&\
  pip-compile requirements.in --resolver=backtracking &&\
  pip install -r requirements.txt