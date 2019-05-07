# Using-Neo4j-CQL--Graph-Database

open an excel file

add the below text to the first 3 columns of the the 1st row:

https://en.wikipedia.org/wiki/Neo4j	Neo4j	/wiki/Neo4j


press F11 to open the macro window

copy paste the code from the attachment with name macro.txt

run the macro




CQL Queries
to delete all nodes

MATCH (n)
OPTIONAL MATCH (n)-[r]-()
DELETE n,r

to check the shortest path between 2 nodes

MATCH (you {title:"Neo4j"})
MATCH (expert)-[:LINK]->(Softwareengineer:node {title:"Software engineer"})
MATCH path = shortestPath( (you)-[:LINK*..5]-(expert) )
RETURN Softwareengineer,expert,path

to view all nodes 

MATCH p=()-[r:LINK]->() RETURN p LIMIT 500
