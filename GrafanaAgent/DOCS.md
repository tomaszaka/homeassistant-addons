# Home Assistant Add-on: Grafana Agent

## Installation

Follow these steps to get the add-on installed on your system:

1. Navigate in your Home assistant to frontend to **Supervisor** -> **Add-on Store**
2. Add additional repository
3. Find the "Grafana agent" add-on and click it.
4. Click on the "INSTALL" button.

## How to use

1. Set the *bearer*, *target*, *url*, *username* and *password*. These fields is mandatory.
2. Start the add-on.
3. Check the add-on log output to see the result.
4. Add `prometheus:` to your Home Assistant configuration. More information how to configure Prometheus in Home Assistant can be found here: https://www.home-assistant.io/integrations/prometheus/

## Add-on Configuration

The Grafana agent add-on can be tweaked to your likings. This section
describes each of the add-on configuration options.

Example add-on configuration:

bearer: >-
  long-live_home_assistant_token
target: home_assistant_ip:port
url: prometheus_url_remote_write
username: prometheus_username_remote_write
password: >-
  prometheus_url_remote_write
scrape_int: 1m
log_level: info


### Option: `bearer` (required)

This is Home Assistant long lived token that can be generated in **Profile**, under Long-Lived Access Token select **Create Token**.

### Option: `target` (required)

If Home Assistant is not configured to work SSL, then internal IP:PORT can be defined here, otherwise please use FQDN:PORT.

### Option: `url` (required)

Remote Write Endpoint URL that should be taken from Grafana Cloud Prometheus component.

### Option: `username` (required)

Username / Instance ID that should be taken from Grafana Cloud Prometheus component.

### Option: `password` (required)

Password / API key that should be takne from Grafana Cloud Prometheus component.

### Option: `scrape_int` (optional)

This is scrape interval. By default it is set to 1m.

### Option: `log_level` (optional)

By default it is set to **info**. In Add-on logs you will be able to see only info level logs.
To investigate issues it's wise to change log_level to get more information.

Possible options:
**info** - Only write logs at info level or above
**warn** - Only write logs at the warn level or above.
**error** - Only write logs at the error level.
**debug** - Write all logs, including debug level logs.

## Home Assistant Configuration

Grafana agent will be used to pull metrics from prometheus component and send metrics to Grafana Cloud. For more information about setting prometheus in Home Assistant configuration.yaml, see the prometheus documentation for Home Assistant.

Example Home Assistant configuration:

```yaml
prometheus:
  namespace: homeassistant
```

## Support

Got questions?

In case you've found a bug, please [open an issue on my GitHub][issue].

[issue]: https://github.com/tomaszaka/homeassistnat-addons/Grafana-Agent/issues
[repository]: https://github.com/hassio-addons/repository