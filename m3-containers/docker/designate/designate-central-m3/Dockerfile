FROM hub.global.cloud.sap/monsoon/ubuntu-source-designate-central:stable-mitaka

MAINTAINER andrew.battye@sap.com

USER root
RUN apt-get -y update
RUN apt-get -y install python-mysqldb

RUN apt-get install -y python-psycopg2 postgresql-client && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
