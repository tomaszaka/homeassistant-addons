ARG BUILD_FROM GRAFANA_FROM
FROM ${BUILD_FROM}

ADD  ${GRAFANA_FROM} /tmp/
ADD rootfs /
RUN dpkg -i /tmp/grafana-agent-0.31.3-1.amd64.deb \
&& rm /tmp/grafana-agent-0.31.3-1.amd64.deb \
&& chmod a+x /etc/s6-overlay/s6-rc.d/grafanaAgent/*
