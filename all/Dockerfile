FROM python:3.11.2-slim as build

RUN set -ex \
  && apt-get -y update \
  && apt-get -y install --no-install-recommends git \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR /opt/octodns

COPY requirements.txt all-requirements.txt

ARG OCTODNS_FLAVOR=octodns

RUN set -ex; \
  if [ "${OCTODNS_FLAVOR}" != "octodns" ] ; \
  then head -n1 all-requirements.txt >> requirements.txt; \
  grep "${OCTODNS_FLAVOR}" all-requirements.txt >> requirements.txt; \
  else \
  cp all-requirements.txt requirements.txt; \
  fi

RUN set -ex \
  && python -m venv env \
  && . env/bin/activate \
  && pip install --no-cache-dir -r requirements.txt

ENV PATH=/opt/octodns/env/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

CMD [ "/bin/sh" ]
