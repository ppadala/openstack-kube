FROM hub.global.cloud.sap/monsoon/ubuntu-source-cinder-api:stable-mitaka
MAINTAINER andrew.battye@sap.com

USER root
# install the metrics middleware
RUN /var/lib/kolla/venv/bin/pip --no-cache-dir install git+https://github.com/sapcc/raven-python.git
RUN /var/lib/kolla/venv/bin/pip --no-cache-dir install git+https://github.com/sapcc/openstack-ops-middleware.git

# and the modified paste.ini that has the metrics middleware in it
COPY api-paste.ini /etc/cinder/
USER cinder
