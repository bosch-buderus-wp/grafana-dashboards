# Grafana Dashboards for Bosch/Buderus heat pumps

Grafana dashboards for Bosch Compress 5800/6800i & Buderus Logatherm WLW176/186 heat pumps.

## Live view with ems-esp

This dashboard presents the current status of the heat pump in a nice overview along with essential metrics regarding its total runtime.

It exclusively retrieves data using [ems-esp](https://bosch-buderus-wp.github.io/docs/smarthome/) with the [Infinity](https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/) datasource.

![ems-esp Live View (light)](/images/grafana-emsesp_light.png)
[ems-esp Live View (dark)](/images/grafana-emsesp_dark.png)

To use this dashboard with your already running ems-esp, start by installing [Infinity](https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/) in your locally running Grafana instance.
Once installed, navigate to _Dashboards_, select _New_ then _Import_ and and paste the contents of either the [light configuration](/dashboards/grafana-dashboard-emsesp_light.json) or the [dark configuration](/dashboards/grafana-dashboard-emsesp_dark.json) into the text field.

The dashboard has been tested with ems-esp version 3.7.1 with a Bosch CS6800i.
If you prefer to obtain values from InfluxDB rather than ems-esp, simply modify the panel queries accordingly.
All queries are named after the corresponding entity from ems-esp (list of [entity names](https://bosch-buderus-wp.github.io/docs/smarthome/entities)).
If you encounter any issues or have suggestions for improvements, please feel free to open an issue.

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
