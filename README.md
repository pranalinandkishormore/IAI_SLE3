Empirical Performance Analysis of BFS and DFS

1. Project Title

Empirical Performance Analysis of BFS and DFS

2. Course Details

- Course: Introduction to Artificial Intelligence
- Course Code: 02AML204
- Student Name: Pranali Nandkishor More
- PRN: 25UAM132
- Division: B
- Department: CSE (AI & ML)
- Institute: DKTE

3. Project Description

This project implements and empirically compares two fundamental graph traversal algorithms:

- Breadth-First Search (BFS)
- Depth-First Search (DFS)

The project measures the performance of both algorithms using execution time and the number of nodes expanded. Different goal nodes are used to observe the behavior of BFS and DFS under different search conditions.

The project also uses profiling scripts to analyze the execution performance of the search algorithms.

4. Objectives

The main objectives of this project are:

1. To implement BFS using a queue.
2. To implement DFS using a stack.
3. To use a visited set to avoid repeated node traversal.
4. To measure the execution time of BFS and DFS.
5. To count the number of nodes expanded.
6. To compare the performance of BFS and DFS.
7. To analyze best, average, and worst-case behavior.
8. To generate profiling results for both algorithms.

5. System Structure

graph TD
    User["User / Developer"] -->|Runs script| System["BFS & DFS Benchmarking System"]

    System --> BFS["bfs.py<br/>Breadth-First Search"]
    System --> DFS["dfs.py<br/>Depth-First Search"]

    BFS --> Graph["Shared Graph Structure<br/>Adjacency List"]
    DFS --> Graph

    System --> Profile["Profiling Scripts"]
    Profile --> Results["Performance Results"]

6. Repository Structure

IAI_SLE2_BFS_DFS/
│
├── bfs.py
├── dfs.py
├── bfs_for_pyspy.py
├── dfs_for_pyspy.py
├── profile_bfs.py
├── profile_dfs.py
├── bfs_profile.svg
├── dfs_profile.svg
├── .gitignore
├── README.md
└── CONTRIBUTION.md

File Description

File| Purpose
"bfs.py"| Contains Breadth-First Search implementation
"dfs.py"| Contains Depth-First Search implementation
"bfs_for_pyspy.py"| BFS script prepared for profiling
"dfs_for_pyspy.py"| DFS script prepared for profiling
"profile_bfs.py"| Measures and profiles BFS performance
"profile_dfs.py"| Measures and profiles DFS performance
"bfs_profile.svg"| BFS profiling output
"dfs_profile.svg"| DFS profiling output
".gitignore"| Specifies files ignored by Git
"README.md"| Project documentation
"CONTRIBUTION.md"| Contribution and work record

7. BFS Algorithm

Breadth-First Search explores the graph level by level.

Working

1. Start from the given start node.
2. Insert the start node into a queue.
3. Remove a node from the front of the queue.
4. Check whether it is the goal node.
5. If not, visit its unvisited neighbors.
6. Add unvisited neighbors to the queue.
7. Repeat until the goal is found or the queue becomes empty.

Data Structures Used

- Queue using "deque"
- Visited set
- Adjacency list

8. DFS Algorithm

Depth-First Search explores one branch as deeply as possible before backtracking.

Working

1. Start from the given start node.
2. Insert the start node into a stack.
3. Remove a node from the top of the stack.
4. Check whether it is the goal node.
5. If not, add its unvisited neighbors to the stack.
6. Continue until the goal is found or the stack becomes empty.

Data Structures Used

- Stack using Python list
- Visited set
- Adjacency list

9. Benchmarking

The project compares BFS and DFS using:

- Minimum execution time
- Average execution time
- Maximum execution time
- Number of nodes expanded

The "timeit" module is used to obtain repeated execution measurements.

The general flow is:

Start
  ↓
Initialize graph
  ↓
Select start and goal node
  ↓
Run BFS / DFS
  ↓
Measure execution time
  ↓
Count nodes expanded
  ↓
Repeat measurements
  ↓
Calculate min / average / max
  ↓
Compare results

10. Profiling

Profiling is performed to understand where the program spends its execution time.

The profiling scripts are:

profile_bfs.py
profile_dfs.py

The generated profiling results are stored as:

bfs_profile.svg
dfs_profile.svg

These results help identify the performance characteristics of BFS and DFS.

11. Level-Wise Execution Flow

graph TD
    A[Start: Initialize Queue or Stack with Start Node] --> B{Is container empty?}
    B -- Yes --> C[Return total nodes_expanded]
    B -- No --> D[Pop node from container]
    D --> E{Is node == goal?}
    E -- Yes --> C
    E -- No --> F[Iterate through neighbors]
    F --> G{Is neighbor unvisited?}
    G -- Yes --> H[Mark as visited & Push to container]
    G -- No --> F
    H --> B

12. Expected Comparison

Parameter| BFS| DFS
Basic structure| Queue| Stack
Traversal| Level-wise| Depth-wise
Memory usage| Can be higher| Usually lower
Shortest path in unweighted graph| Yes| Not guaranteed
Suitable for| Finding nearby/shortest-level nodes| Exploring deep paths

The actual execution performance depends on the graph structure and selected goal node.

13. Technologies Used

- Python
- Git
- GitHub
- timeit
- PySpy / profiling tools
- Mermaid diagrams

14. How to Run

Clone the repository:

git clone https://github.com/juishinde136-arch/IAI_SLE2_BFS_DFS.git

Move into the project directory:

cd IAI_SLE2_BFS_DFS

Run BFS:

python bfs.py

Run DFS:

python dfs.py

Run BFS profiling:

python profile_bfs.py

Run DFS profiling:

python profile_dfs.py

15. Conclusion

This project provides an empirical comparison of BFS and DFS using execution time and nodes expanded as performance measures.

BFS explores nodes level by level using a queue, while DFS explores nodes deeply using a stack. The benchmarking and profiling results help understand how the two algorithms behave for different search conditions.

The project demonstrates the practical application of graph search algorithms and performance analysis in Artificial Intelligence.

16. Repository

GitHub Repository:

https://github.com/juishinde136-arch/IAI_SLE2_BFS_DFS 
