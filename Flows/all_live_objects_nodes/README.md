# All Live Objects nodes
![the flow view1](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/all_live_objects_nodes/img/img1.png?raw=true)
![the flow view2](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/all_live_objects_nodes/img/img2.png?raw=true)
![the flow view3](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/all_live_objects_nodes/img/img3.png?raw=true)

## Flow description

This flow presents all of the Live Objects nodes we offer with our Node-RED SaaS Enabler. Thanks to them Node-RED and Live Objects can be integrated really easily.

![send-enrich-receive](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/all_live_objects_nodes/img/img4.png?raw=true)

To simplify the Node-RED and LiveObjects integration, we developed a set of LiveObjects nodes.

Using these, you can **send, enrich or receive** data to/from LiveObjects.

- Use the external connector node to send new data from Node-RED to LiveObjects.

- In order to enrich data coming from LiveObjects, utilise the Custom Pipeline nodes. There are in and out nodes for starting and closing pipelines respectively.

- If you want to receive data from LiveObjects as they arrive, make use of the FIFO node or HTTP Push nodes. The FIFO queue releases messages only when your flow is up and running, so you won’t miss any data when using it.

### More info

For more precise instructions please check out the nodes' descriptions (double click on a node in the editor).