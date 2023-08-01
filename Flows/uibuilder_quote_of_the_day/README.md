# Frontend application with UiBuilder
![fronted view](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img1.png?raw=true)

## Flow description

This flow shows how to create and host frontend application on Node-RED using UiBuidler nodes. 
Before you start you need to install UiBuidler module from Node-RED Pallete.

## How to setup this flow

- Go to the bottom of this page and copy flow
- Import flow to your Node-RED (ctrl+i)
![imported flow](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img2.png?raw=true)
- Open UiBiulder (Simple Example) node and replace "my_endpoint" with your endpoint if needed  `note that all endpoints must start with "ui/"`
![uibuilder endpoint](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img3.png?raw=true)
- After that click done and then click Save to deploy your flows
- In this example flow you can see 4 comment nodes at the top. You need to open index.html, index.js and index.css comments, copy their contents and paste them to uiBuilder node. There should be some default content inside uibuilder files, you need to delete them
![comment html](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img4.png?raw=true)
![index.html copied](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img5.png?raw=true)
- After pasting each file content you will see "Save Required". You need to 
**click Save** next to Reset button inside UiBuidler node to apply changes
- Then go back to the Core tab and click Open button to see if it works
![open button](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img6.png?raw=true)
- You should see you web page up and running
![web page](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img7.png?raw=true)
- Then you can go back to your Node-RED and click inject node, you will see qoute of the day on your page
![finall result](https://github.com/DatavenueLiveObjects/Node-RED-FAQ-examples/blob/master/Flows/uibuilder_quote_of_the_day/img/img1.png?raw=true)


[credit](https://flows.nodered.org/flow/bbe6803d9daebda5c991336cf4e5e3e0)