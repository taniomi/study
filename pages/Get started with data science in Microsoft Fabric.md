## Learning objectives
	- Understand the data science process
	- Train models with notebooks in Microsoft Fabric
	- Track model training metrics with MLflow and experiments
- # Introduction
	- **Data science** is a combination of mathematics, statistics, and computer engineering.
	- You can use data science to create **artificial intelligence (AI)** models that encompass the complicated patterns you find in your data.
	- A common approach is to use data science to train **machine learning (ML)** models using libraries like `scikit-learn` in Python to achieve AI.
	- In this module, you learn about a typical data science project. Additionally, you explore which Microsoft Fabric features you can use for each part of the data science process.
- # Understand the data science process
	- Extract insights or predictions from the data. Visualization is the most common way. Data scientists can use statistics and mathematics as tools to find patterns invisible through visualization alone.
	- Though training the model is important, it's not the only task in a data science project. Before exploring a typical data science process, let's explore common machine learning models you can train.
- ## Explore common machine learning models
	- The purpose of ML is to find patterns in data through the training of models.
	- Four common types of ML models are shown below:
		- ![machine-learning-tasks.png](../assets/machine-learning-tasks_1748444608753_0.png)
		- **Classification**: Predict a categorical value like whether a customer may churn.
		  logseq.order-list-type:: number
		- **Regression**: Predict a numerical value like the price of a product.
		  logseq.order-list-type:: number
		- **Clustering**: Group similar data points into clusters or groups.
		  logseq.order-list-type:: number
		- **Forecasting**: Predict future numerical values based on time-series data like the expected sales for the coming month.
		  logseq.order-list-type:: number
	- To choose a model for training, you first need to understand the business problem and the data available.
- ## Understand the data science process
	- Common processes for training a model:
		- ![data-science-process.png](../assets/data-science-process_1748444764317_0.png)
		-