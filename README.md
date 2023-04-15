Simple Grafana dashboard for MyElectricalData

Written for influxDB v2, with flux language. It needs you to configure a datasource in grafana pointing to your InfluxDB server. I named my datasource "InfluxDB2". Not sure if it's critical for the dashboard to work.

Does not use the PDL as variable in the queries, so removed that as a variable. It pulls all data in InfluxDB assuming a single PDL

To use, simply go to grafana, on the left pick Dashboard, Import, then select the JSON file

Give the dashboard a name and voilà
