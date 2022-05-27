Not a very interesting subject this time around, it's simply a couple of logistic problems that can be solved with graph algos and in not necesarilly efficient ways.

The first task is to find the shortest path from a deposit to a store and back, pretty much just apply a shortest path algorithm twice, once for deposit to store and once for store to deposit (as we're dealing with directed graphs).

After that we're supposed to find strongly connected components between stores. The course hasn't taught us Kosaraju or Tarjan, so I just went with Warshall to get the road matrix and just formed the components from there on.

Lastly, the third task wanted the shortest path that starts from any deposit, visits all nodes in a strongly connected graph and returns to the same deposit, allowing traversal through other deposits as well, but not other nodes. The solution to this problem was kinda sorta explained, as in it was hinted what you were supposed to do without many details regarding the implementation. The proposed idea was to modifiy Dijkstra so that it creates the distances from a node to every other node, while also keeping track of which nodes had been visited through a bitmask.
