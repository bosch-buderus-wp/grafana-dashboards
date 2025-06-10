# Grafana Dashboards for Bosch/Buderus heat pumps

Grafana dashboards for Bosch Compress 5800/6800i & Buderus Logatherm WLW176/186i heat pumps.

## Live view with ems-esp

This dashboard presents the current status of the heat pump in a nice overview along with essential metrics regarding its total runtime.

It exclusively retrieves data using [ems-esp](https://bosch-buderus-wp.github.io/docs/smarthome/) with the [Infinity](https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/) datasource, eliminating the need to set up a database like InfluxDB.

![ems-esp Live View (light)](/images/grafana-emsesp_light.png)
[ems-esp Live View (dark)](/images/grafana-emsesp_dark.png)

To use this dashboard with your already running ems-esp, start by installing [Infinity](https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/) in your locally running Grafana instance.
Once installed, navigate to _Dashboards_, select _New_ then _Import_ and and paste the contents of either the [light configuration](/dashboards/grafana-dashboard-emsesp_light.json) or the [dark configuration](/dashboards/grafana-dashboard-emsesp_dark.json) into the text field.

Dashboards configurations:

- Light Theme: [grafana-dashboard-emsesp_light.json](/dashboards/grafana-dashboard-emsesp_light.json)
- Dark Theme: [grafana-dashboard-emsesp_dark.json](/dashboards/grafana-dashboard-emsesp_dark.json)

The dashboard has been tested with ems-esp version 3.7.1 with a Bosch CS6800i.
If you prefer to obtain values from InfluxDB rather than ems-esp, simply modify the panel queries accordingly.
All queries are named after the corresponding entity from ems-esp (list of [entity names](https://bosch-buderus-wp.github.io/docs/smarthome/entities)).
If you encounter any issues or have suggestions for improvements, please feel free to open an issue.

## Additional historic data with InfluxDB

If you already store the entities of your ems-esp in an InfluxDB, you can extend your dashboard with historic data visualizations.
In addition to the live view above, the following dashboard provides a section with various visualizations depending on the selected time interval.

![ems-esp+influxDB Dashboard (light)](/images/grafana-dashboard-emsesp-influxdb_light.png)
[ems-esp+influxDB Dashboard (dark)](/images/grafana-dashboard-emsesp-influxdb_dark.png)

Dashboard configurations:

- Light Theme: [grafana-dashboard-emsesp-influxdb_light.json](/dashboards/grafana-dashboard-emsesp-influxdb_light.json)
- Dark Theme: [grafana-dashboard-emsesp-influxdb_dark.json](/dashboards/grafana-dashboard-emsesp-influxdb_dark.json)

The InfluxQL queries assume that each entity is stored in a measurement table with the name of the ems-esp entity, e.g. `nrgtotal`:

| time                | item     | value |
| ------------------- | -------- | ----- |
| 1711055880009000000 | nrgtotal | 44.81 |
| 1711055940009000000 | nrgtotal | 44.84 |
| 1711056000008000000 | nrgtotal | 44.87 |

If your InfluxDB is organized in a different structure, you might need to adapt the InfluxQL queries.

Additional dashboards featuring historical data sourced from InfluxDB will be available soon.

## Contributing

Contributions are welcome! If you'd like to add more dashboards or visualizations, please submit a pull request.

## License

This project is licensed under the MIT License.
See the [LICENSE](./LICENSE) file for details.

## Acknowledgments

- https://grafana.com
- https://emsesp.org
- https://www.svgrepo.com
- https://excalidraw.com
- https://svgtoexcalidraw.com
