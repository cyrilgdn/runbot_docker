FROM camptocamp/odoo-project:9.0-1.5.0
MAINTAINER Camptocamp

RUN apt-get update && apt-get install -y git nginx && apt-get clean

COPY requirements.txt /opt/odoo/requirements.txt
RUN pip install -r /opt/odoo/requirements.txt

RUN chown -R 999 /opt/odoo/external-src/odoo-extra/runbot/static/repo

ENV ADDONS_PATH="/opt/odoo/external-src/odoo-extra,/opt/odoo/external-src/runbot-addons,/opt/odoo/src/addons"
