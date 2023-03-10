![Version](https://img.shields.io/badge/dynamic/yaml?label=Version&query=%24.version&url=https://raw.githubusercontent.com/tomaszaka/homeassistant-addons/main/GrafanaAgent/config.yaml)
![arch](https://img.shields.io/badge/dynamic/yaml?color=success&label=Arch&query=%24.arch&url=https://raw.githubusercontent.com/tomaszaka/homeassistant-addons/main/GrafanaAgent/config.yaml)
## About

---

The Grafana Agent is a telemetry collector for sending metrics, logs, and trace data to the opinionated Grafana observability stack.

It is commonly used as a tracing pipeline, offloading traces from the application and forwarding them to a storage backend. The Grafana Agent tracing stack is built using OpenTelemetry.

## Installation

---

The installation of this add-on is pretty straightforward and not different in comparison to installing any other add-on.

1. Add my add-ons repository to your home assistant instance (in supervisor addons store at top right, or click button below if you have configured my HA)
   [![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Ftomaszaka%2Fhomeassistant-addons)
2. Install this add-on.
3. Click the `Save` button to store your configuration.
4. Set the add-on options to your preferences
5. Start the add-on.
6. Check the logs of the add-on to see if everything went well.

## Configuration

---

## Add-on Configuration

The Grafana agent add-on can be tweaked to your likings. This section
describes each of the add-on configuration options.

Example add-on configuration:
```yaml
bearer: >-
  long-live_home_assistant_token
target: home_assistant_ip:port
url: prometheus_url_remote_write
username: prometheus_username_remote_write
password: >-
  prometheus_url_remote_write
scrape_int: 1m
log_level: info
```

## Support

Create an issue on github
[repository]: https://github.com/tomaszaka/homessistant-addons
