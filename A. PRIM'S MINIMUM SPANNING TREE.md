# PRIM'S MINIMUM SPANNING TREE

## PROGRAM STATEMENT:

To find the sum of weights of the edges of the M inimum Spanning Tree

![image](https://github.com/user-attachments/assets/1178ac25-7edf-4ac9-a32e-4f6d32f4db72)

## ALGORITHM:  

1.	Start the program.
2.	Initialize a priority queue to store edges, each represented by (weight, vertex).
3.	Choose an arbitrary starting vertex and mark it as visited.
4.	Add all edges connected to the starting vertex into the priority queue.
5.	While the priority queue is not empty, pop the edge with the minimum weight and if the destination vertex is not in the MST, add it and update the priority queue with edges from the newly visited vertex.
6.	End the program by calculating the sum of the edge weights in the MST.

## PROGRAM:
```

void Graph::addEdge(int u, int v, int w)
{
adj[u].push_back(make_pair(v, w)); adj[v].push_back(make_pair(u, w));
}
 ```
## OUTPUT :
![image](https://github.com/user-attachments/assets/584c8e46-7ded-44d3-9342-e25404ed4f76)

## RESULT:

Thus, the C++ program to find the sum of weights of the edges of the Minimum Spanning Tree is created successfully.

