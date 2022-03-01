# Live Objects FIFO Queue In simple example
![the flow view](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/fifo_in_simple/img/img1.png?raw=true)
## Flow description

Put your valid API key with an Application profile and FIFO name (same as in LO) to the fifo node and save the flow.

Under the node, there should be a green dot indicating the node is properly connected and receives buffered data.

As soon as the node connects to LO, it receives all the buffered data from the queue (if any).

You can see the content of messages in the debug console.

## Node description
### In Live Objects
Configure a FIFO queue in Live Objects. To make use of the queue, specifiy routes in the Routing Tab. 
### In Node-RED
The name of your queue has to be entered in the node parameters. You need to enter also an **API key** with an **Application** profile.

Live Objects FIFO queue broadcasts data messages only if there is an active recipient. When the FIFO node is disconnected or improperly configured, it doesn't receive data, however Live Objects puts them into a buffer. All the buffered data will be processed on the next valid connection of the node. Live Objects FIFO queue data is sent over MQTT protocol.