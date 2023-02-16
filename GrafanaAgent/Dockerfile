ARG BUILD_FROM
ARG GRAFANA_FROM
FROM ${BUILD_FROM}

ADD  https://github.com/grafana/agent/releases/download/v0.31.3/${GRAFANA_FROM} /tmp/
ADD rootfs /
RUN dpkg -i /tmp/${GRAFANA_FROM} \
# && rm /tmp/grafana-agent-0.31.3-1.amd64.deb \
&& chmod a+x /etc/s6-overlay/s6-rc.d/grafanaAgent/*
