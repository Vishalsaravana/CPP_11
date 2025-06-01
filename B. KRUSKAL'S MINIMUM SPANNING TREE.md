# KRUSKAL’S MINIMUM SPANNING TREE

## PROGRAM STATEMENT:
Given a houses of a city consisting of N 2D coordinates {x, y} where each coordinate represents the location of each house, the task is to find the minimum cost to connect all the houses of the city.

![image](https://github.com/user-attachments/assets/7d25cf7c-dc1b-473b-8ec5-97058e5deb1c)

## ALGORITHM:  

1.	Start the program.
2.	For each pair of houses, compute the Euclidean distance between them and store it as an edge with weight (distance).
3.	Use Kruskal's algorithm or Prim's algorithm to find the Minimum Spanning Tree (MST).
4.	Sort the edges by their weight (increasing order).
5.	Use a Union-Find (Disjoint-Set) data structure to detect and avoid cycles while adding edges to the MST.
6.	The sum of the selected edges' weights in the MST will give the minimum cost to connect all houses.
7.	End the program.

## PROGRAM:
```

voidaddEdge(int x, int y, int w)
{
edgelist.push_back({ w, x, y});
}
 ```

## OUTPUT :
![image](https://github.com/user-attachments/assets/b0621a29-c737-4c1d-b4bf-8329e8164b80)

## RESULT:
Thus, the C++ program to find the minimum cost to connect all the houses of the city Tree is created successfully.

