ARG BUILD_FROM
FROM ghcr.io/hassio-addons/ubuntu-base/amd64:8.2.1

ADD  https://github.com/grafana/agent/releases/download/v0.31.3/grafana-agent-0.31.3-1.amd64.deb /tmp/
ADD rootfs /
RUN dpkg -i /tmp/grafana-agent-0.31.3-1.amd64.deb \
&& rm /tmp/grafana-agent-0.31.3-1.amd64.deb \
&& chmod a+x /etc/s6-overlay/s6-rc.d/grafanaAgent/*
