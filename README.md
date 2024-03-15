# BitNodes-Snapshot API Documentation

## Overview

The BitNodes-Snapshot API provides access to the latest snapshot of the active nodes of the Bitcoin network. This API is designed to fetch network snapshots, providing detailed information about the active nodes, including their IP addresses, ports, and other relevant data.

## API Endpoints

### Fetch the Latest Network Snapshot

- **Endpoint:** `/snapshots/latest`
- **Method:** `GET`
- **Tags:** `Snapshots`
- **Summary:** Fetch the latest network snapshot and provide the node details of the active nodes.
- **Responses:**
- `200 OK`: Successful fetching of network snapshot.
- `401 Unauthorized`: Authentication is required to access the resource.
- `429 Too Many Requests`: Too many requests in 24 hours.
- `500 Internal Server Error`: An internal server error occurred.

### Response Schema

The response for the `/snapshots/latest` endpoint includes the following fields:

- `timestamp`: The timestamp of the snapshot in Unix time.
- `total_nodes`: The total number of active nodes in the snapshot.
- `latest_height`: The latest block height in the snapshot.
- `nodes`: An array of objects, each representing a node with details such as IP address, port, version, services, last seen, last sent, last received, country, country code, region, region name, city, zip code, latitude, longitude, timezone, ASN, and organization.

## Example Response

json { "timestamp": 1710282079, "total_nodes": 18515, "latest_height": 834418, "nodes": [ { "91.209.51.131:8333": [ 70016, "/Satoshi:0.21.0/", 1710345617, 1033, 834540, "131.51.209.91.it-tv.org", 834542, "UA", 50.4522, 30.5287, "Europe/Kyiv", "AS48239", "Scientific-Production Enterprise Information Technologies Ltd" ] } ] }

## Additional Information

- **API Documentation:** For more detailed information and additional endpoints, refer to the [BitNodes API Documentation](https://bitnodes.io/api/).
- **BitNodes Project:** Learn more about the BitNodes project and its mission to provide real-time information on the Bitcoin peer-to-peer network at [BitNodes](https://bitnodes.io/).
- **Bitnodes Snapshot Open API documentation:** For more detailed information regarding the snapshot endpoints, refer to the [Bitnodes Snapshot Open API documentation](https://app.swaggerhub.com/apis/RakshithRajkumar/Active-Nodes-Snapshot/1.0.0).
