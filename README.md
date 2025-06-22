# Grafana Dashboards for Bosch/Buderus heat pumps

Grafana dashboards for Bosch Compress 5800/6800i & Buderus Logatherm WLW176/186i heat pumps.

- ems-esp only: [ Live view & total statistics](#live-view-with-ems-esp)
- ems-esp + InfluxDB (selectable interval):
  - [Power consumption & heat output](#power-consumption--heat-output)
  - [Daily consumption](#daily-consumption)
  - [DHW profile](#dhw-profile)
  - [Sustainability: CO<sub>2</sub> emissions & share of renewables](#sustainability)

## Live view with ems-esp

This dashboard presents the current status of the heat pump in a nice overview along with essential metrics regarding its total runtime.

It exclusively retrieves data using [ems-esp](https://bosch-buderus-wp.github.io/docs/smarthome/) with the [Infinity](https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/) datasource, eliminating the need to set up a database like InfluxDB.

![ems-esp Live View (light)](/images/grafana-emsesp_light.png)
[ems-esp Live View (dark)](/images/grafana-emsesp_dark.png)

To use this dashboard with your already running ems-esp, start by installing [Infinity](https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/) in your locally running Grafana instance.
Once installed, navigate to _Dashboards_, select _New_ then _Import_ and paste the contents of either the [light configuration](/dashboards/grafana-dashboard-emsesp_light.json) or the [dark configuration](/dashboards/grafana-dashboard-emsesp_dark.json) into the text field.

Dashboards configurations:

- Light Theme: [grafana-dashboard-emsesp_light.json](/dashboards/grafana-dashboard-emsesp_light.json)
- Dark Theme: [grafana-dashboard-emsesp_dark.json](/dashboards/grafana-dashboard-emsesp_dark.json)

The dashboard has been tested with ems-esp version 3.7.1 with a Bosch CS6800i.
If you prefer to obtain values from InfluxDB rather than ems-esp, simply modify the panel queries accordingly.
All queries are named after the corresponding entity from ems-esp (list of [entity names](https://bosch-buderus-wp.github.io/docs/smarthome/entities)).
If you encounter any issues or have suggestions for improvements, please feel free to open an issue.

## Power consumption & heat output

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

The dashboard requires the following entities to be stored in the InfluxDB:

- [_metertotal_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#mit-2-nachkommastellen): if not available, try [_nrgconstotal_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#ohne-nachkommastellen)
- [_nrgtotal_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#mit-2-nachkommastellen): if not available, try [_nrgsupptotal_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#ohne-nachkommastellen)
- [_meterheat_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#mit-2-nachkommastellen): if not available, try [_nrgconscompheating_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#ohne-nachkommastellen)
- [_dhw.meter_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#mit-2-nachkommastellen): if not available, try [_dhw.nrgconscomp_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#ohne-nachkommastellen)
- [_outdoortemp_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#messwerte)
- [_hpcurrpower_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#leistung)
- [_curburnpow_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#status)
- [_curtemp2_](https://bosch-buderus-wp.github.io/docs/smarthome/entities#messwerte-1)

### Daily consumption

If you are interested in daily electricity consumption for heating and domestic hot water, the following visualization is also included in the above dashboard.

![ems-esp+influxDB Dashboard Additions (light)](/images/grafana-dashboard-emsesp-influxdb-additions_light.png)
[ems-esp+influxDB Dashboard Additions (dark)](/images/grafana-dashboard-emsesp-influxdb-additions_dark.png)

### DHW profile

If you’re curious about how much your domestic hot water (DHW) temperature drops and when the heating system kicks in, the dashboard also includes a visualization for this information (screenshot provided above).

### Sustainability

Furthermore, the dashboard contains a section for sustainability with 2 visualizations:

![ems-esp+influxDB Dashboard Sustainability (light)](/images/grafana-dashboard-emsesp-influxdb-sustainability_light.png)
[ems-esp+influxDB Dashboard Sustainability (dark)](/images/grafana-dashboard-emsesp-influxdb-sustainability_dark.png)

- _Daily CO<sub>2</sub> emissions of the heat pump compared to a gas heating system:_ \
  This visualization requests the current CO<sub>2</sub> emissions of the consumed electricity in Germany (DE-LU) from [www.greengrid-compass.eu](https://www.greengrid-compass.eu).
  The CO<sub>2</sub> of the gas heating system can be adjusted in the dashboard variable `$ref_heating_emissions`.
  In the legend of the visualization you can see, how much CO<sub>2</sub> the heat pump has saved in the selected interval.
  In the screenshot, the heat pump produced 128 kgCO<sub>2</sub>eq compared to a gas heating which produced 282 kgCO<sub>2</sub>eq - more than twice the amount.

- _Share of renewable energy:_ \
  This visualization requests the share of renewable energy in the German (DE-LU) energy consumption mix from [www.greengrid-compass.eu](https://www.greengrid-compass.eu).
  In the legend you can also see the share of renewable energy weighted by electricity consumed by your heat pump.
  In the screenshot the mean renewable share for the whole German electricity consumption was 50.2% in the observation interval.
  The shown heat pump consumed in average 47.1% renewables.

To use both visualizations, you have to create a free API key on [api-portal.eco2grid.com](https://api-portal.eco2grid.com/get-started) and add the API key as dashboard variable `$api_key_ggc` in Grafana.

Please note that the visualizations assume that you solely use electricity from the grid - no own solar power.

Additional dashboards featuring historical data sourced from InfluxDB will be available soon.

## FAQ

**Q: I'm seeing "Field not found" errors in the visualizations. What can I do?**

A: This usually indicates that Grafana can't reach your ems-esp gateway.
Ensure that your ems-esp is running and accessible on your network.
You can configure the ems-esp host by setting the Grafana variable `emsesp_host` in the Grafana dashboard settings.
By default, it is configured to `http://ems-esp`.

**Q: My visualizations, which use the InfluxDB, do not present any data. How can I fix this?**

A: This error can occur if the entity names used in the Grafana panel queries do not exactly match the names stored in your InfluxDB or if your InfluxDB does not contain a dedicated measurement per entity.
In these cases, simply adapt the queries according to your InfluxDB schema.

## Contributing

Contributions are welcome! If you'd like to add more dashboards or visualizations, please submit a pull request.

## License

This project is licensed under the MIT License.
See the [LICENSE](./LICENSE) file for details.

## Acknowledgments

- https://grafana.com
- https://emsesp.org
- https://www.bosch-homecomfort.com
- https://www.buderus.de/de/waermepumpe
- https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/
- https://www.greengrid-compass.eu/
- https://www.svgrepo.com
- https://excalidraw.com
- https://svgtoexcalidraw.com
