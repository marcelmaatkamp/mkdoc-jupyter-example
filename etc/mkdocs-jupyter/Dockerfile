ARG MKDOCS_MATERIAL_VERSION
FROM marcelmaatkamp/mkdocs-jupyter-example-jupyter:${JUPYTER_VERSION}

COPY requirements.in requirements.in
RUN \
  pip install --upgrade \
    pip \
    pip-tools &&\
  pip-compile requirements.in  --resolver=backtracking --max-rounds 20 --verbose &&\
  pip install -r requirements.txt

COPY material /docs/material 
COPY docs /docs/docs 
COPY mkdocs.yml /docs/mkdocs.yml