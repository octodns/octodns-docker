FROM python:3.10-slim as build
RUN set -ex \
  && apt-get -y update \
  && apt-get -y install --no-install-recommends git \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# FROM python:3.10-slim
# COPY --from=build /usr/local/lib/python*/site-packages /usr/local/lib/python3.10/site-packages
# COPY --from=build /usr/local/bin/octodns-* /usr/local/bin/
CMD [ "/bin/sh" ]
