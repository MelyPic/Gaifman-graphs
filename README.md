# Gaifman-graphs
The program FromFileToGraph.py:
Reads the dataset and constructs the desire Gaifman graph.

Construction of Gaifman graph.
In the current version each attribute value read is a vertex in the graph,
using the function: TxtFile_ValueEqualAttribute(filename_ext,GraphMatrix).

To the correct construction of the titanic graph, you must to add the way to read the data,
choosing to read it with the function: TxtFile(filename_ext, GraphMatrix)
 
Construction of standard Gaifman graph:
To construct the graph with just connected or disconnected items, 
you must select the option: 7.Plain Gaifman graph 
 
Construction of exponential Gaifman graph.
In the current version of the exponential Gaifman graph the equivalence relations
are calculated as floor(log(c_{i,j},2)), where c_{i,j} is the multiplicity of the co-occurrences of i and j, 
that leads to lose the cases where is just one co-occurrence.
We have the option to calculate it as ceil(log(c_{i,j}+1,2)) in order to preserve that co-occurrence,
to use one or another depends on how representative is to keep it.  
