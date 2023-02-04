ARG MKDOCS_MATERIAL_VERSION
FROM squidfunk/mkdocs-material:${MKDOCS_MATERIAL_VERSION}

RUN \
 apk update &&\
 apk add \
    g++ \
    build-base

COPY requirements.in requirements.in
RUN \
  pip install --upgrade \
    pip \
    pip-tools &&\
  pip-compile requirements.in  --resolver=backtracking --max-rounds 20 --verbose &&\
  pip install -r requirements.txt

RUN  pip install -r requirements.txt
COPY material /docs/material
COPY docs /docs/docs
COPY mkdocs.yml /docs/mkdocs.yml