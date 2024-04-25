# Markov-Chain-Page-Rank-Analysis
 
This project aims to enhance my knowledge of Markov Chains and the Page Rank taught in Module 11 in CSE6040. An Airline's transportation infrastructure can viewed in form of a graph or a network in which vertices are airports and edges are the direct-flight segments that connect them.

In this analysis I aim to answer to answer the following questions for an airline business utilizing Markov Chains or in other text's the famous PageRank Algorithm by Google:

1. Which vertices/nodes in the network have high inbound/outbound demand ?
2. Which vertices/nodes in the network have high ticket revenues?
3. What is the most profitable route in our network ?


As state in notebook 11, the 'importance' of an airport is traditionally associated with its volume of inbound and outbound connections. In graph lingo, this connectivity measure is known as the degree of a vertex or node. The indegree is the number of incoming edges to a node, while the outdegree is the number of outgoing edges. However, in our analysis, I tried to depart from this approach alittle and instead utilize metrics such as ticket revenue, number of flights and passengers in a particular route(edge) to assess an airport's significance. While inbound and outbound degrees are valuable indicators, they may not fully capture an airport's importance. My analysis aims to provide an assessment of airport importance by incorporating various metrics an airline business may have beyond traditional connectivity measures.


Reasoning behind the choice of metrics

1. Counting Flights: Counting the number of flights for each route provides insights into the frequency of travel between airports which is 
   useful for understanding the volume of traffic on different routes and identifying popular or high-demand routes.
2. Counting Passengers: Counting the number of passengers for each route gives a more direct measure of passenger demand and traffic flow 
   between airports and considers the number of individuals traveling on each route, which is essential for understanding passenger 
   behavior, market demand, and revenue potential.
3. Counting Revenue: Counting the total revenue generated for each route provides insights into the financial performance and profitability 
   of different routes. This approach considers the revenue generated from ticket sales.

This notebook takes inspiration from the following links please use these resources for deeper understanding of the concepts in this notebook:
1. A paper by MongoDB Interns : https://www.mongodb.com/blog/post/pagerank-on-flights-dataset
2. CSE 6040 Notebook 11 and CSE 6040 Final Exam Practice Problem 2
3. A Medium article on Markov Chains and PageRank : https://medium.com/towards-data-science/brief-introduction-to-markov-chains-2c8cab9c98ab
4. Online Literature on PageRank by Larry Page


I will be making use of a Kaggle SQLlite database linked here : https://www.kaggle.com/datasets/saadharoon27/airlines-dataset
The tables include :aircrafts_data,airports_data,boarding_passes,bookings,flights,seats,ticket_flights,tickets.
(Aggreates of this tables have been loaded to meet size contraints for submission)

The notebook makes use of SQL and Python Pandas, Numpy , SciPy and Matplotlib skills for Exploratory Data Analysis and in the end I will build a PageRank Algorithm. Project Steps :

1. Data Loading: Loading the relevant databases and tables required for the analysis.
2. Data Cleaning: Preparing the data by performing necessary cleaning procedures to ensure its quality and reliability for analysis.
                  Historical Data Insights: Extracting insights from historical data to address the listed business questions, gaining an 
                  understanding of past trends and patterns.
3. PageRank Analysis: Utilizing PageRank algorithm to uncover insights and rank elements based on their importance within the network, 
                      addressing specific business questions.
4. Comparison of Rankings: Conducting a comparative analysis between historical rankings and those derived from PageRank (a form of Markov 
                            Chain), highlighting differences and identifying which method provides more valuable insights for the business.
