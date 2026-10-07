# Network Analysis of Character Interactions in *The Hobbit*

*Group project (5 members). This folder contains my analysis notebook.*

## Question
**Which characters hold the story of *The Hobbit* together?**

## Data
- Undirected, unweighted network of **41 characters** and **160 interactions**
- Source: [charnet – hobbit.dat](https://github.com/aholanda/charnet/blob/master/data/hobbit.dat)
- Place the file at `data/Hobbit_Data.xlsx`

## Method
- Network density, mean degree and connected components
- Degree, closeness and betweenness centrality
- k-core decomposition and clique detection

## Key results
- **Bilbo** has the most connections (degree 26): the story's social hub
- **Thorin** has the highest betweenness centrality (0.43): the bridge that connects different groups
- Low density (19.5%) but one connected component, consistent with "small-world" literary networks

## Files
- `hobbit_network_analysis.ipynb` – analysis in Python (NetworkX)
