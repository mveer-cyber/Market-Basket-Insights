# Market-Basket-Insights

Market Basket Insights

Overview:

This notebook is part of a project focused on market basket analysis. We will begin by loading and preprocessing the dataset.
Dataset 
The dataset is stored in the file Assignment-1_Data.xlsx located. It contains information related to market transactions.
Loading the Dataset
Let's start by loading the dataset into a DataFrame using pandas.
Initial Exploration
We'll perform an initial exploration of the dataset to understand its structure and characteristics.

Preprocessing:

We'll preprocess the data to ensure it's ready for analysis.
Formatting the transaction data in a suitable format for analysis
Developing the preprocessed data into analysis. Split the 'Itemname' column in transaction_data into individual items using str.split(', ', expand=True).Concatenate the original DataFrame (transaction_data) with the items DataFrame (items_df) using pd.concat.Drop the original 'Itemname' column since individual items are now in separate columns.Display the resulting DataFrame.

Association Rules - Data Mining:
Converting Items to Boolean Columns:

To prepare the data for association rule mining, we convert the items in the transaction_data DataFrame into boolean columns using one-hot encoding. This is achieved through the pd.get_dummies function, which creates a new DataFrame (df_encoded) with boolean columns representing the presence or absence of each item.

Association Rule Mining:
We apply the Apriori algorithm to perform association rule mining on the encoded transaction data. The min_support parameter is set to 0.007 to filter out infrequent itemsets. The resulting frequent itemsets are then used to generate association rules based on a minimum confidence threshold of 0.5.Finally, we print the generated association rules.

Visualization:
Visualizing Market Basket Analysis Results:

We use matplotlib and seaborn libraries to create a scatterplot visualizing the results of the market basket analysis. The plot depicts the relationship between support, confidence, and lift for the generated association rules.
Interactive Network Visualization for Association Rules
We utilize the NetworkX and Plotly libraries to create an interactive network graph visualizing the association rules. This graph represents relationships between antecedent and consequent items, showcasing support as edge weights.

Interactive Sunburst Chart for Association Rules:
We use Plotly Express to create an interactive sunburst chart visualizing association rules. This chart represents the relationships between antecedent and consequent items, showcasing lift as well as support through color intensity.
