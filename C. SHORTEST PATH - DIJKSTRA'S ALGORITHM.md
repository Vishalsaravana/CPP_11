# SHORTEST PATH - DIJKSTRA'S ALGORITHM

## PROGRAM STATEMENT:

There is a directed weighted connected graph. You are given a positive integer n which denotes that the graph has n nodes labeled from 1 to n, and an array edges where each edges[i] = [ui, vi, weighti] denotes that there is an edge between nodes ui and vi with weight equal to weighti.

Correct the given C++ function to find the dijkstra'a shortest path from every node to all other nodes in the given graph.

![image](https://github.com/user-attachments/assets/7a807033-c0c1-4e80-bffe-1ff17b1442f2)

## ALGORITHM:  

1.	Start the program.
2.	Initialize the distance for the source vertex to 0 and all other vertices to infinity.
3.	Insert the source vertex into a set with its distance as the key.
4.	While the set is not empty:
a.	Extract the vertex with the minimum distance from the set.
b.	For each neighboring vertex, check if the current path offers a shorter distance than previously known. If so, update the distance and insert it back into the set.
5.	After processing all vertices, print the shortest distance from the source to each vertex.
6.	End the program.
 
## PROGRAM:
```

// Printsshortest paths fromsrc to allother vertices void Graph::shortestPath(int src)
{
set< pair<int, int> > setds; vector<int> dist(V, INF); setds.insert(make_pair(0, src)); dist[src] = 0;
while(!setds.empty())
{
pair<int, int> tmp =*(setds.begin()); setds.erase(setds.begin());


int u=tmp.second;
list< pair<int, int> >::iterator i;
for (i= adj[u].begin(); i != adj[u].end(); ++i)
{
int v= (*i).first;
intweight =(*i).second;
if(dist[v] >dist[u] + weight)
{
if(dist[v] != INF)
setds.erase(setds.find(make_pair(dist[v], v))); dist[v] = dist[u] + weight; setds.insert(make_pair(dist[v], v));
}
}
}

// Print shortest distances stored in dist[] printf("Vertex Distance from Source\n"); for (int i= 0; i< V; ++i)
printf("%d %d\n", i, dist[i]);
}
 
```
## OUTPUT :
![image](https://github.com/user-attachments/assets/955dd265-d32e-4edc-9ad2-84a65e539383)

## RESULT:

Thus, the C++ program to find the dijkstra'a shortest path from every node to all other nodes in the given graph is created successfully

