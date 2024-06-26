---
id: io-influxdb-sink
title: InfluxDB sink connector
sidebar_label: "InfluxDB sink connector"
original_id: io-influxdb-sink
---

The InfluxDB sink connector pulls messages from Pulsar topics
and persists the messages to InfluxDB.

## Configuration

The configuration of the InfluxDB sink connector has the following properties.

### Property

| Name | Type|Required | Default | Description
|------|----------|----------|---------|-------------|
| `influxdbUrl` |String| true|" " (empty string) | The URL of the InfluxDB instance. |
| `username` | String|false| " " (empty string) |The username used to authenticate to InfluxDB. |
| `password` | String| false|" " (empty string)  | The password used to authenticate to InfluxDB. |
| `database` |String| true | " " (empty string)| The InfluxDB to which write messages. |
| `consistencyLevel` | String|false|ONE | The consistency level for writing data to InfluxDB. <br /><br />Below are the available options:<li>ALL<br /></li><li> ANY<br /></li><li>ONE<br /></li><li>QUORUM </li>|
| `logLevel` | String|false| NONE|The log level for InfluxDB request and response. <br /><br />Below are the available options:<li>NONE<br /></li><li>BASIC<br /></li><li>HEADERS<br /></li><li>FULL</li>|
| `retentionPolicy` | String|false| autogen| The retention policy for InfluxDB. |
| `gzipEnable` | boolean|false | false | Whether to enable gzip or not. |
| `batchTimeMs` |long|false| 1000L |   The InfluxDB operation time in milliseconds. |
| `batchSize` | int|false|200| The batch size of writing to InfluxDB. |

### Example

Before using the InfluxDB sink connector, you need to create a configuration file through one of the following methods.

* JSON

  ```json

  {
      "influxdbUrl": "http://localhost:8086",
      "database": "test_db",
      "consistencyLevel": "ONE",
      "logLevel": "NONE",
      "retentionPolicy": "autogen",
      "gzipEnable": false,
      "batchTimeMs": 1000,
      "batchSize": 100
  }

  ```

* YAML

  ```yaml

  configs:
      influxdbUrl: "http://localhost:8086"
      database: "test_db"
      consistencyLevel": "ONE"
      logLevel: "NONE"
      retentionPolicy: "autogen"
      gzipEnable: false
      batchTimeMs: 1000
      batchSize: 100

  ```

