
#Python API for analyzing and manipulating genotype-phenotype maps

This package defines a standard data-structure for genotype-phenotype (GP) map data.
Useful for creating network graphs (via NetworkX) from GP data. Subset, manipulate,
extend, etc. GP maps. Calculate statistics, model evolutionary trajectories, predict
phenotypes (in combination with the epistasis package). Efficient memory usage,
using numpy arrays to store in memory.

## Basic example

Import the package's base object.
```python
import GenotypePhenotypeMap
```

Load a dataset from disk.
```python
gpm = GenotypePhenotypeMap.from_json("data.json")
```

Create a NetworkX graph from the genotype-phenotype map data.
```python
import networkx as nx

gpm.add_network()
G = gpm.Graph
nx.draw(G)
```

## Installation

To install this package, clone from source and use pip.
```
git clone https://github.com/harmslab/seqspace
cd seqspace
pip install -e .
```

## Dependencies

The following modules are required. Also, the examples/tutorials are written in Jupyter notebooks and require IPython to be install.

* [NetworkX](https://networkx.github.io/)
* [Numpy](http://www.numpy.org/)
