FROM jupyter/datascience-notebook:2023-01-30

USER root

# RUN \
#  apt update &&\
#  apt install -y \
#   libgl1-mesa-glx \
#   xvfb

USER jovyan
ARG SQLALCHEMY_VERSION
RUN \
 pip install \
   ipython-sql \
   psycopg2-binary \
   SQLAlchemy==${SQLALCHEMY_VERSION} \
   matplotlib \
   seaborn \
   plotly \
   matplotlib \
   pyvista \
   ipyvtklink \
   ipympl \
   ipycanvas \
   pythreejs \
   ipygany \
   itkwidgets