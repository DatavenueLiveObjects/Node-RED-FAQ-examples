# Data enrichment with Custom Pipeline nodes example
![the flow view](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/custom_pipeline_enrichment_simple/img/img1.png?raw=true)

## Flow description

In *Custom Pipeline In* node specify an **endpoint** you want to send data to.

*Enriching function* node modifies the payload. Virtually any group of nodes can be used to influence the data as long as the `msg.payload` meets the LO criteria at the end.

The *Custom Pipeline Out* node sends the `msg.payload` back to Live Objects.

More about LO data transformation [HERE](https://liveobjects.orange-business.com/doc/html/lo_manual_v2.html#DATA_TRANSFORMATION).