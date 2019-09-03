# Gaifman-graphs
The main program that you have to run is OutpDotFile.py:

At first you have to select the data entry.(Go FromFileToGraph.py to read some details)

Then you can select the variation of Gaifman graph you want to work.(Go FromFileToGraph.py to read some details)  

To replay the examples try:

1 -> mushroomTr_2000.txt -> 7.Plain Gaifman graph 
1 -> mushroomTr_2000.txt -> 2.Thresholded graph -> 1000
1 -> mushroomTr_2000.txt -> 2.Thresholded graph -> 800
1 -> mushroomTr_2000.txt -> 6.Exponential Gaifman graph -> 0 -> 0
1 -> zoo4.arff -> 3.Linear graph -> 0 -> 0 -> 10
1 -> votesTr_100.txt -> 3.Linear graph -> 0 -> 0 -> 100

*You have to change the way to read titanic in ReadFile function on file FromFileToGraph.py
1 -> titanic.txt -> 7.Plain Gaifman graph 
1 -> titanic.txt -> 2.Thresholded graph -> 1000


FromFileToGraph.py:
Reads the dataset and constructs the desired Gaifman graph.

Construction of Gaifman graph.
In the current version each attribute value read is a vertex in the graph,
using the function: TxtFile_ValueEqualAttribute(filename_ext,GraphMatrix).

To the correct construction of the titanic graph, you must to modify the way to read the data,
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

FindUnionDecompositionV8.py:
Here we apply the 2-structure decomposition algorithm to obtain the strong clan tree. 
