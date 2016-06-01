#Why Use Data Visualization?

## Thats a simple question to answer with a few bullet points:
-	It will help you understand data.
-	It will allow you to take segment data and perform engineering to create features.
-	It will allow you to build models, which combine tuned algorithms, existing data, and features to create recipes for awesomeness.

## What does it look like from a workflow perspective?

Understand the data -> Pick out relevant information -> Build a model -> Deploy the model.

-	Throughout this whole pipeline, data visualization can be really important tool to helping you understand everything from what's in the data itself to how you're manipulating that data, how a model is working and performing, and then how a service is working and performing in terms of things like latency and through-put.

##Viusalizing Data with React.js

Rendering visual elements, maintaining interactivity, and then keeping track of state suddenly became easy when I started using React.js Below is a pipeline for Data Visulation.
-	DATA ->Aggregation ->Visual Elements ->Rendering ->Rendered Visualization

##Deeper understanding of the pipeline

-	Data Aggregation
    -The first step of aggregation or data reduction is designing and optimizing a data pipeline that will reduce a large block of data into a form you can ship over to a browser.

    -You want to compute close ot the data. Think for a second that you have a powerful server  with a large amount of data on it and a really, really tiny pipe to a web browser. The web browser is where everything is ultimately going to get displayed, but you can't just ship over all of that data. If you try to push all the data through that very tiny pipe it may cause the browser to crash.Do the data reduction where the data is:

##The Flux Architecture

I will demonstrate a quick workflow of what you want to achieve.

Action ->Dispatcher ->Store ->View ->Action ->Send back to Dispatcher & Repeat Process.

To accomplish this data reduction, we use an architecture that is flux-like. You use the dispatcher and a store component. Dispatcher's responsibile for taking actions and making changes in the store. The store is essentially responsible for being the single source. Everything flows from the store into the view, which acutally renders on the page. Overall this helps you keep organized of state changes throughout the application.

Here is another more detailed workflow using GraphLab Canvas:

Action ->XHR/WebSocket ->Stateful Server ->View -> Action ->Loop back to XHR/Websocket & Repeat the process.

You can see that dispatcher has been replaced with xml http request and/or web socket, so essentially we're crossing the wire over the network for every action. Store has been changed to a stateful object on the server which simplifies state management quite a bit because we don't have to keep anything in sync across the client and server.
	

