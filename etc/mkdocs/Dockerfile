FROM squidfunk/mkdocs-material:9.0.10

RUN \
 apk update &&\
 apk add \
    g++ \
    build-base

ARG SQLALCHEMY_VERSION
RUN \
  pip install \
    mkdocs-jupyter \
    SQLAlchemy==${SQLALCHEMY_VERSION} \
    matplotlib \
    seaborn

COPY material /docs/material 
COPY docs /docs/docs 
COPY mkdocs.yml /docs/mkdocs.yml