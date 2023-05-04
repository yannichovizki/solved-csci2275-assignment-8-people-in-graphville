Download Link: https://assignmentchef.com/product/solved-csci2275-assignment-8-people-in-graphville
<br>
<h1>People in Graphville</h1>

You are the mayor of Graphville. You have a list of all the people in your town. You also know the relation between them, basically if they know each other. You need to increase the community interaction between your constituents. Now before you do that you need to know a lot of other details like if two people know each other directly or through a friend or in any other way, also how many groups are there in your town.

<strong>What your program needs to do:</strong>

<strong>Build a graph.</strong> There is a file on canvas called people.txt that contains the names of people and with them the names of people they know similar to an adjacency list. When the user starts the program, read in the file and build a graph where every person is a vertex, and there is an edge for every person they know.

For this assignment, you are building the graph and implementing functionalities given in the menu.

<strong>Use a command-line argument to handle the filename.</strong>

<strong>Display a menu.</strong> Once the graph is built, your program should display a menu with the following options:

<ol>

 <li><strong>Print list of people and their acquaintances </strong></li>

 <li><strong>Print if people know each other </strong></li>

 <li><strong>Print groups </strong></li>

 <li><strong>Find the least number of introductions required </strong></li>

 <li><strong>Quit </strong></li>

</ol>

<strong>Menu Items and their functionality:</strong>

<ol>

 <li><strong>Print list of people.</strong> If the user selects this option, the vertices and adjacent vertices should be displayed.</li>

 <li><strong>Print if people know each other.</strong> This option takes two vertices as user inputs and displays True is the vertices are adjacent, and False if they are not adjacent.</li>

</ol>

If this is a part of the file:

Akhil-Paramvir,Aurangzeb

Aurangzeb-Akhil,Kieran

Earl-Paramvir,Kieran,Zack

Then Earl and Zack know each otherKieran and Aurangzeb know each otherand so on.

<ol start="3">

 <li><strong>Print groups.</strong> If the user selects this option, you need to do a depth-first search (DFS) of the graph to determine the connected people in the graph, and assign those cities the same group ID. The connected people are the vertices that are connected, either directly by an edge, or indirectly through another vertex. For example, in the above example, Akhil is connected to Kieran via Aurangzeb. When assigning group Ids, start at the first vertex and find all vertices connected to that vertex. This is group 1. Next, find the first vertex that is not assigned to group 1. This vertex is the first member of group 2, and you can repeat the depth-first search to find all vertices connected to this vertex. Repeat this process until all vertices have been assigned to a group.</li>

 <li><strong>Find the least number of introductions required-</strong> If the user selects this option, they should be prompted for the names of two names. Your code should first determine if they are in the same group. If the people are in different groups, print “No way to introduce them”. If the people are in the same group, run a breadth-first search (BFS) that returns the number of vertices to traverse along the shortest path,</li>

</ol>

and the names of the vertices along the path. For example,

For Akhil and Paramvir no one else is required as they are directly connected. But Kieran and Akhil can be introduced via Aurangzeb.

So your output should be something like :

1, Aurangzeb




If there were N people in between then output:

N, Name1-Name2-…..-NameN