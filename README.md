Simple Grafana dashboard for MyElectricalData

Written for influxDB v2, with flux language. It needs you to configure a datasource in grafana pointing to your InfluxDB server. I named my datasource "InfluxDB2". Not sure if it's critical for the dashboard to work.

Does not use the PDL as variable in the queries, so removed that as a variable. It pulls all data in InfluxDB assuming a single PDL

To use, simply go to grafana, on the left pick Dashboard, Import, then select the JSON file

Give the dashboard a name and voilà

Screenshots:

<img width="1406" alt="Screenshot 2023-04-15 at 11 46 21" src="https://user-images.githubusercontent.com/97752752/232206461-d0a5a9b5-2c09-4115-934a-9db6d9957f57.png">
<img width="1410" alt="Screenshot 2023-04-15 at 11 46 34" src="https://user-images.githubusercontent.com/97752752/232206469-df600929-9c39-4066-80f1-bf12b53cf13f.png">
<img width="1409" alt="Screenshot 2023-04-15 at 11 46 41" src="https://user-images.githubusercontent.com/97752752/232206473-292d4d7f-e36a-4fac-ba2e-20d29f85592a.png">
