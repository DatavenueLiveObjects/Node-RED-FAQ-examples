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

```
[{"id":"2bf61e781b720ef1","type":"tab","label":"X-CONNECTOR MULTI SIMPLE","disabled":false,"info":""},{"id":"224d84c03f5ebde3","type":"inject","z":"2bf61e781b720ef1","name":"Send data as external connector \"abcd\"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"connector/v1/nodes/abcd/data","payload":"{\"value\":{\"data\":1234}}","payloadType":"json","x":230,"y":200,"wires":[["0f13eabe3693cf82"]]},{"id":"0f13eabe3693cf82","type":"external-connector-out-multiple","z":"2bf61e781b720ef1","name":"LO external connector out multiple","apikey":"a4066115947b4b669a4401a42980525e","x":700,"y":260,"wires":[]},{"id":"c10ebc3609c93757","type":"inject","z":"2bf61e781b720ef1","name":"Send data as external connector \"dcba\"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"connector/v1/nodes/dcba/data","payload":"{\"value\":{\"data\":1234}}","payloadType":"json","x":230,"y":260,"wires":[["0f13eabe3693cf82"]]},{"id":"c85b59ef4ba34053","type":"inject","z":"2bf61e781b720ef1","name":"Send data as external connector \"efgh\"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"connector/v1/nodes/efgh/data","payload":"{\"value\":{\"data\":1234}}","payloadType":"json","x":230,"y":320,"wires":[["0f13eabe3693cf82"]]},{"id":"5da36def055e806a","type":"comment","z":"2bf61e781b720ef1","name":"In order to send data to LO as multiple external connectors dynamically, a specific message topic must be set","info":"","x":430,"y":80,"wires":[]},{"id":"b2a222c62f31aa77","type":"comment","z":"2bf61e781b720ef1","name":"msg.topic = \"connector/v1/nodes/{external_ID}/data\"","info":"","x":250,"y":120,"wires":[]},{"id":"9339c30f1b1432f7","type":"comment","z":"2bf61e781b720ef1","name":"Double click on the node to see instructions","info":"","x":720,"y":220,"wires":[]},{"id":"ea528f123e13f5a0","type":"comment","z":"2bf61e781b720ef1","name":"Double click on nodes to see the msg format","info":"","x":230,"y":160,"wires":[]}]
```