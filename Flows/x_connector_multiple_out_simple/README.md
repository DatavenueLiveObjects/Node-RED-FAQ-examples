# External connector out multiple simple example
![the flow view](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/x_connector_multiple_out_simple/img/img1.png?raw=true)

## Flow description

Put your valid API key with an external connector profile to the LO node and run the inject nodes. 

Optionally you can change the payload.value and topic.

See how new x-connector devices and data appear in your LO dashboard.  

## Node description
LO External Connector Out Multiple node acts as a MQTT client. It connects and sends payload to LO in the external connector mode. 

Use an **API key** with an **External Connector** profile generated in Live Objects.

The ID (name) of the connector has to be specified in the message topic as follows:
`msg.topic = "connector/v1/nodes/{externalID}/data"`.

To send data, include it in the payload: `msg.payload = {"value":{"yourDataA":1234, "yourDataB":"text"}}`.

If the externalID is not recognized by LO a new connector device is created.

It takes approx. 100-200ms to process a message. The node has FIFO message queue implemented, thus you can feed it with multiple messages and then one after another will get processed. 