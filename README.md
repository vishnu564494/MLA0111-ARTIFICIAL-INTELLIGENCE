def bfs(graph, start):
    visited = set()          
    queue = deque([start])  

    visited.add(start)

    while queue:
        node = queue.popleft()   # Dequeue
        print(node, end=" ")

        # Visit all neighbors
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)
