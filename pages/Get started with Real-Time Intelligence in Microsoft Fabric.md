- [Module](https://learn.microsoft.com/en-us/training/modules/get-started-kusto-fabric/)
- [Badge]()
- ## Learning Objectives
	- Understanding core concepts related to real-time data analytics.
	- Understanding  Microsoft Fabric's Real-Time Intelligence capabilities.
	- Exploring core components of Real-Time Intelligence in Microsoft Fabric.
	- Ingesting real-time data by using an *eventstream*.
	- Using an *eventhouse* and a KQL database for real-time data analysis in Microsoft Fabric.
	- Visualizing data in *real-time dashboards*.
	- Using *Activator* in Microsoft Fabric to define alerts that trigger automated actions.
- # Introduction
	- Two patterns for data analytics:
		- **Batch data analytics**, in which data is loaded into an analytical data store at periodic intervals as a batch operation; enabling historical analysis of data from past events.
		- **Real-time data analytics**, in which data from events is ingested in real-time (or *near* real-time) as events occur in a *stream* of data that can be analyzed, visualized, and used to trigger automated responses.
	- Implementing real-time data analytics through *lambda* architecture that combines the periodic loading of batch data for historical analysis with the ingestion of data streams for real-time analysis.
- # What is real-time data analytics?
	- *Stream processing* of data sends data continually, to create (near) real-time visualizations, graphs, KPIs.
	- It can be used for monitoring purposes of for triggering automated actions based on certain conditions.
	- > **Stream processing** the integer equivalent of **batch processing**.
	- Common goals for real-time analytics include:
		- Continuously analyzing data to report issues or trends.
		- Understanding component or system behavior under various conditions to help plan future enhancements.
		- Triggering specific actions or alerts when certain events occur or thresholds are exceeded.
- ### Characteristics of real-time data analytics solutions
	- Stream processing solutions for real-time data analytics
	- Common characteristics:
		- A data stream is *unbounded* - data is added to the stream perpetually.
		  logseq.order-list-type:: number
		- Data records in the stream typically include *temporal* (time-based) data indicating when the event to which the record relates occurred (or was recorded).
		  logseq.order-list-type:: number
		- Aggregation of streaming data is often performed over temporal *windows* - for example, recording the number of social media posts per minute or the average rainfall per hour.
		  logseq.order-list-type:: number
		- The results of streaming data processing can be used to support real-time (or *near* real-time) automation or visualization, or persisted in an analytical store to be combined with other data for historical analysis. Many solutions combine these approaches to support both real-time and historical analytics.
		  logseq.order-list-type:: number
		- ![stream-processing.png](../assets/stream-processing_1748007884182_0.png)
- # Real-Time Intelligence in Microsoft Fabric
	-