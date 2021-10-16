# Grafana Dashboard for qBittorrent

<img src="https://github.com/caseyscarborough/qbittorrent-grafana-dashboard/blob/master/images/logo.png" width=100>

This repository contains a Grafana dashboard for qBittorrent using Prometheus.

It integrates with [qbittorrent-exporter](https://github.com/caseyscarborough/qbittorrent-exporter).

View it on [Grafana Community Dashboards](https://grafana.com/grafana/dashboards/15116).

## Features

It shows the following metrics:

- All time download/upload
- Session download/upload
- Cumulative upload/download speeds
- Global ratio/download speed/upload speed
- App version
- Torrent list with statuses
- Total torrents/seeders/leechers
- Torrent state chart
- Amount remaining by torrent
- Incomplete torrent progress
- Download/upload speed by torrent

## Requirements

This dashboard requires [grafana-piechart-panel](https://grafana.com/grafana/plugins/grafana-piechart-panel/) for some panels. You can install by running any of these:

```bash
# Grafana CLI
grafana-cli plugins install grafana-piechart-panel

# Download and unzip manually
wget -nv https://grafana.com/api/plugins/grafana-piechart-panel/versions/latest/download -O grafana-piechart-panel.zip
unzip -q grafana-piechart-panel.zip -d .
mv grafana-piechart-panel /var/lib/grafana/plugins/grafana-piechart-panel
rm grafana-piechart-panel.zip

# Clone the Git repo
git clone https://github.com/grafana/piechart-panel.git --branch release-1.6.1
mv piechart-panel /var/lib/grafana/plugins/grafana-piechart-panel
```

Restart your Grafana server after installing the plugin.

## Screenshots

![](https://github.com/caseyscarborough/qbittorrent-grafana-dashboard/blob/master/images/top.png)

![](https://github.com/caseyscarborough/qbittorrent-grafana-dashboard/blob/master/images/bottom.png)