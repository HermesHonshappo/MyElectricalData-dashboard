**Simple Grafana dashboard for MyElectricalData**

Written for influxDB v2, with flux language. It needs you to configure a datasource in grafana pointing to your InfluxDB server. I named my datasource "InfluxDB2". Not sure if it's critical for the dashboard to work.

Does not use the PDL as variable in the queries, so removed that as a variable. It pulls all data in InfluxDB assuming a single PDL

The below is assuming you already have a data connection in Grafana to your influxDB database, and the proper plugins installed. If not, see at the bottom

To use, simply go to grafana, on the left pick Dashboard, Import, then select the JSON file

Give the dashboard a name and voilà

Screenshots:

<img width="1406" alt="Screenshot 2023-04-15 at 11 46 21" src="https://user-images.githubusercontent.com/97752752/232206461-d0a5a9b5-2c09-4115-934a-9db6d9957f57.png">
<img width="1410" alt="Screenshot 2023-04-15 at 11 46 34" src="https://user-images.githubusercontent.com/97752752/232206469-df600929-9c39-4066-80f1-bf12b53cf13f.png">
<img width="1409" alt="Screenshot 2023-04-15 at 11 46 41" src="https://user-images.githubusercontent.com/97752752/232206473-292d4d7f-e36a-4fac-ba2e-20d29f85592a.png">

**Installing the connection to InfluxDB**

You need to go to grafana settings -> administration -> data sources and add a data source. Pick influx as the engine.
Then fill the URL of the database, organization ID and token that you have generated in InfluxDB

<img width="698" alt="Screenshot 2023-07-08 at 15 40 42" src="https://github.com/HermesHonshappo/MyElectricalData-dashboard/assets/97752752/16019f1f-fd1a-4a89-ab48-83ab0702300c">
<img width="609" alt="Screenshot 2023-07-08 at 15 42 20" src="https://github.com/HermesHonshappo/MyElectricalData-dashboard/assets/97752752/4a536550-b228-4194-8404-c05183d80b09">

**Installing plugins**

You need the two plugins below installed. Go to settings -> administration -> plugins and install them if missing
<img width="1108" alt="Screenshot 2023-07-08 at 15 43 51" src="https://github.com/HermesHonshappo/MyElectricalData-dashboard/assets/97752752/2fee1ab1-62ee-49bf-87bd-7df55bec6298">

<img width="1300" alt="Screenshot 2023-07-08 at 15 44 25" src="https://github.com/HermesHonshappo/MyElectricalData-dashboard/assets/97752752/54f8d1e1-a83b-40c0-ba8c-159ad0199e00">

**Changelog**

2023-07-08 update:
1) modified .JSON file since it had link to an influxDB UID. For a brand new install, the UID would not match
2) added link & screenshots of the two plugins to install
3) added screenshot of install for influxDB connector

2024-06-17 update:
1) Added primary energy factor. Used for energy classification of house in France
2) current and previous years are now computed automatically. Should not need an update each year
3) current year % is now based on same consumption the year before (Jan1st to current date vs Jan1st 1 year ago vs 1 year ago today)
