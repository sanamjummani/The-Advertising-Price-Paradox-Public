# Data

## Dataset — Tropicana Orange Juice Sales Panel

The dataset used in this analysis is the Tropicana subset of the **Dominick's Finer Foods retail scanner database**, maintained by the James M. Kilts Center for Marketing at the University of Chicago Booth School of Business.

### What it contains

| Field | Description |
|---|---|
| `sales` | Weekly unit sales volume per store |
| `price` | Retail price per carton in USD |
| `feat` | Binary indicator — 1 if the product was featured in the weekly ad circular, 0 otherwise |

**9,649 weekly store-level observations** covering Tropicana brand orange juice across multiple Dominick's store locations.

### Why it is not included here

The raw data file is not included in this repository in line with academic data sharing guidelines. The Dominick's dataset is publicly available for research purposes through the Kilts Center at the University of Chicago.

If you want to reproduce the analysis, the dataset can be accessed at:
[https://www.chicagobooth.edu/research/kilts/datasets/dominicks](https://www.chicagobooth.edu/research/kilts/datasets/dominicks)

Once downloaded, place the Tropicana file in this folder and rename it `oj_tropicana.csv`. The notebook will run without any other changes.

### About Dominick's Finer Foods

Dominick's was a Chicago-area grocery chain that collected detailed point-of-sale scanner data across its stores throughout the 1990s. The dataset has been widely used in academic marketing research for over two decades and is considered a benchmark for retail pricing and consumer behavior studies.
