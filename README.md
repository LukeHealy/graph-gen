# graph-gen
Pseudo random graph adjacency list and heuristic list generator written in python 2.7. Used to generate test data.

It randomly assigns coordinates, according to the x and y maximums provided.
It then takes the "nodes" it has created, and randomly pairs them with others, without duplicates, thus forming an edge.
The cost between the two is generated using the pythagoras theorum.
The heuristic is generated much the same, but in relation to the node in question and the destination node. (Euclidean distance heuristic.)

### Usage

~~~
python gg.py <x> <y> <num_nodes> <max_branch> <src> <dst>
~~~

### Output

The program outputs the number of nodes, and edges generated.
The adjacency list is saved in a file in the following format: `src  dst cost`.

For example:

~~~
3 1 5.0
3 2 2.236
1 3 5.0
2 3 2.236
~~~

The heuristic file adopts the following format: `node heuristic`

For example:

~~~
1 5.0
2 2.236
3 0.0
~~~

FYI: These files were generated using `python gg.py 5 5 3 2 1 3`