# SolarEdge node for Node-RED (2)

This is a node for Node-RED to grab data from your SolarEdge inverter.  
You'll need an API key and your site ID. Talk to your solar PV installer if you need these.

This Repository is based on the files of Matt Galloway, but includes more API Commands (See list below)

## Installation

In your Node-RED directory:

```
npm install christophcaina/node-red-contrib-solaredge-2
```

## Usage

This package adds 1 input node and 1 configuration node to Node-RED.

The configuration node defines the site and comprises the following options:

  * **Site ID**: The ID of your site.
  * **API Key**: The API key used to talk to the SolarEdge monitoring API. Must be a site API key, not an account users API key.

The input node comprises the following options:

  * **Site**: The SolarEdge site, defined above.
  * **Command**: The command to run against the SolarEdge monitoring API.
  * **Interval**: The interval, in seconds, between calls to the monitoring API.

### Commands

The following commands are supported:

  * **Details**: This provides the overview of the system, including information such as the name, status, peak power, etc.
  * **Overview**: This provides data such as the lifetime energy output, current power output, etc.
  * **Inventory**: This provides inventory data such as Installed components, Serial Numbers, Firmware-Version, etc.
  * **Environmal Benefits**: This provides information of the Environmental benefits of your Solar Installation such as: equivalent planned trees, saved CO2, SO2 and NOX emissions
  * **Current Power Flow**: Indicates, if your Installation is Importing or Exporting Power

For more information on the commands, see the [SolarEdge monitoring API documentation](http://www.solaredge.com/sites/default/files/se_monitoring_api.pdf).

## License

MIT
