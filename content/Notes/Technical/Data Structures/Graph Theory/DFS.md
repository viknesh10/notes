- A graph traversal algorithm
#### Recursive implementation
```
marked = [False] * G.size()
def dfs_pre(G, v):
	visit(v)
	marked[v] = True
	for w in G.neighbours(v):
		if not marked[w]:
			dfs(G, w)
```
#### Iterative implementation
- Done through a stack ds. 
```
marked = [False] * G.size()
def dfs_iter(G, v):
	stack = [v]
	while len(stack) > 0:
		v = stack.pop()
		if not marked[v]:
			visit(v)
			marked[v] = True
			for w in G.neighbours(v):
				if not marked[w]:
					stack.append(w)
```

- Both iterative and recursive implementations run in O(V + E)
- Recursive implementation is however cleaner and easier to read and hence more commonly preferred
#### Preorder vs Postorder traversal
- Preorder - the order of vertices visited first
- Postorder - the order of vertices which reach a dead end first - as in, the first vertex without a neighbour
```
marked = [False] * G.size()
def dfs_post(G, v):
	marked[v] = True
	for w in G.neighbours(v):
		if not marked[w]:
			dfs(G, w)
	visit(v)
```

- Topological sort is a way of traversing a Directed Acyclic Graph (DAG). A topological sort is the reverse of a DFS Postorder