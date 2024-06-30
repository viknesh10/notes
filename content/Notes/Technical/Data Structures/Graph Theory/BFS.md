- Enables you to find the shortest path from one vertex to every other vertex in the graph
- Done through a queue ds
```
marked = [False] * G.size()
def bfs(G, v):
	queue = [v]
	while len(queue) > 0:
		v = queue.pop(0) // Popping off the first element in the queue
		if not marked[v]:
			visit(v)
			marked[v] = True
			for w in G.neighbours(v):
				if not marked[w]:
					queue.append(w)
```