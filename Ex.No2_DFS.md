# Ex.No: 2  Implementation of Depth First Search
### DATE: 17/02/2024                                                                      
### REGISTER NUMBER : 212221040066
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:
```
graph = {
    '2': ['3', '4'],
    '3': ['5'],
    '4': ['6', '7'],
    '6': [],
    '5': ['6'],
    '7': ['8'],
    '8': []
}
visited = set()  # Set for visited nodes.
def dfs(graph, node):  # Function for DFS
    if node not in visited:
        print(node, end=" ")
        visited.add(node)
        for neighbour in graph[node]:
            dfs(graph, neighbour)
# Driver Code
print("DFS order is")
dfs(graph, '2')
```
### Output:
![image](https://github.com/Jayalakshm1/AI_Lab_2023-24/assets/130430542/856cd830-0d6b-4876-91ea-f95cdc6d1c16)
### Result:
Thus the depth first search order was found sucessfully.
