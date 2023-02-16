ARG BUILD_FROM
ARG BUILD_ARCH
FROM ${BUILD_FROM}

ADD  https://github.com/grafana/agent/releases/download/v0.31.3/grafana-agent-0.31.3-1.${BUILD_ARCH}.deb /tmp/
ADD rootfs /
RUN dpkg -i /tmp/${GRAFANA_FROM} \
# && rm /tmp/grafana-agent-0.31.3-1.amd64.deb \
&& chmod a+x /etc/s6-overlay/s6-rc.d/grafanaAgent/*
