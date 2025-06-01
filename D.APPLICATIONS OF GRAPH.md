# APPLICATION OF GRAPH
## PROGRAM STATEMENT:

A traveller needs to visit all cities from a list, where distances between all cities are known and visited once. What is the shortest possible routes that he visits each city exactly once and returns to the origin city?. Find the TSP solution using CPP function.

![image](https://github.com/user-attachments/assets/7733c0de-c671-44b6-a7c8-005332650805)

## ALGORITHM:  

1.	Start the program.
2.	Initialize a list ver containing all vertices except the starting vertex p.
3.	Set m_p to infinity to store the minimum path weight.
4.	Generate all permutations of the vertices in ver:
a.	For each permutation, calculate the total path weight by traversing through the vertices in the order of the permutation.
b.	Add the weight to complete the cycle by returning to the starting vertex p.
5.	Update m_p with the minimum path weight found.
6.	After checking all permutations, return the minimum path weight.
 
## PROGRAM:
```

int TSP(int p) // implement traveling SalesmanProblem.
{
vector<int> ver; // for(int i= 0; i<V; i++)
{
if(i!=p) ver.push_back(i);
}
int m_p=INT_MAX; // storeminimumweight ofa graph
do {
int cur_pth= 0; int k = p;
for(int i=0;i<(int)ver.size();i++)
{
cur_pth += adjMatrix[k][ver[i]]; k = ver[i];
}
cur_pth+= adjMatrix[k][p];
m_p = min(m_p, cur_pth); // to updatethevalue ofminimumweight
}
while (next_permutation(ver.begin(), ver.end())); return m_p;
}
 ```

## OUTPUT :
![image](https://github.com/user-attachments/assets/9ba89b9b-aec6-45f6-b700-ca346e189f54)

## RESULT:

Thus, the C++ program to find the TSP solution using CPP function is created successfully.

