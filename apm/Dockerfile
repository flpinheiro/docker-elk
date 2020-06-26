ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/apm/apm-server:${ELK_VERSION}
COPY ./config/apm-server.yml /usr/share/apm-server/apm-server.yml
USER root
RUN chown root:apm-server /usr/share/apm-server/apm-server.yml
USER apm-server

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu