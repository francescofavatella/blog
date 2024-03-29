---
layout: post
title:  "Graph Algorithms for Technical Interviews"
---

In this episode Alvin will explain how to implement graph algorithms and how to use them to solve coding challenges.

[Graph Algorithms for Technical Interviews - Full Course](https://www.youtube.com/watch?v=tWVWeAqZ0WU)


<iframe width="560" height="315" src="https://www.youtube.com/embed/tWVWeAqZ0WU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Depth First Search
	stack (LIFO)
		pop to read from the top
		push to add to the top


## Breadth First Search
	queue (FIFO)
		shift to read from the head
		push to add to the tail


## Complexity
```
n = # nodes
e - # edges
Time: O(e)
Space: O(n)
```

## Code

```
const depthFirstPrintIterative = (graph, source) => {
	const stack = [source];

	while(stack.length > 0){
		const current = stack.pop(); // read from the back
		console.log(current);

		for (let neighbour of graph[current]){
			stack.push(neighbour); // add to the back
		}
	}	
};

const depthFirstPrintRecursive = (graph, source) => {
	console.log(current);
	for(let neighbour of graph[source]){
		depthFirstPrintRecursive(graph, neighbour);
	}
};


const breadthFirstPrintIterative = (graph, source) => {
	const queue = [source];

	while(queue.length > 0){
		const current = queue.shift(); // read from the head
		console.log(current);

		for (let neighbour of graph[current]){
			queue.push(neighbour); // add to the back
		}
	}

};

const graph = {
	a: ['c', 'b'],
	b: ['d'],
	c: ['e'],
	d: ['f'],
	e: [],
	f: []
};

depthFirstPrintIterative(graph, 'a'); // abdfce
depthFirstPrintRecursive(graph, 'a'); // abdfce

breadthFirstPrintIterative(graph, 'a'); // acbedf
```

## Bonus: Time complexity

$O(n^2)$ -> nested loop

$O(n \log{n})$ -> sort

$O(n)$

$O(\log{n})$ - binary search

$O(1)$ -> hash map