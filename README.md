Not a very interesting subject this time around, it's simply a couple of logistic problems that can be solved with graph algos.

The first task is to find the shortest path from a warehouse to a store and back, pretty much just apply a shortest path algorithm twice, once for warehouse to store and once for store to warehouse (as we're dealing with directed graphs).

After that we're supposed to find strongly connected components between stores. The course hasn't taught us Kosaraju or Tarjan, so I just used Warshall to get the road matrix and just formed the components from there on.

Lastly, the third task wanted the shortest path that starts from any warehouse, visits all nodes in a strongly connected graph and returns to the same warehouse, allowing traversal through other deposits as well, but not other nodes. The solution to this problem was kinda sorta explained, as in it was hinted what you were supposed to do without many details regarding the implementation. The proposed idea was to modifiy Dijkstra so that it creates the distances from a node to every other node, while also keeping track of which nodes had been visited through a bitmask.
