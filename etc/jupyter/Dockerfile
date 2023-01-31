FROM jupyter/datascience-notebook:2023-01-30

ARG SQLALCHEMY_VERSION
RUN \
 pip install \
   psycopg2-binary \
   SQLAlchemy==${SQLALCHEMY_VERSION} \
   matplotlib \
   seaborn