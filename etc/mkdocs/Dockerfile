FROM squidfunk/mkdocs-material:9.0.8

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