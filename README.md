# SLE-3: Architectural Design Using Full C4 Model

## Course
**02AML204 – Introduction to Artificial Intelligence**

## Student Details
- **Student Name:** Tanishka Vijay Chougule
- **PRN:** 25UAM086
- **Division:** B
- **Program:** SY B.Tech. CSE (AI & ML)
- **Date:** 03/10/2026

## System Title
**BFS vs DFS – Maze Path-Finding Profiling**

## 1. System Description
The BFS vs DFS Maze Path-Finding system compares Breadth-First Search (BFS) and Depth-First Search (DFS) on randomly generated grid mazes.

The system finds paths from a start point to a goal and measures:
- Execution time
- Nodes expanded
- Path length

The results are used to study and compare the behaviour of the two search algorithms.

## 2. C4 Architectural Design

### Level 1 – Context Diagram
Shows the overall BFS vs DFS Maze Path-Finding System and its interaction with the user/input and output/results.

### Level 2 – Container Diagram
1. **Maze Input / Generator** – Generates or accepts the maze used for path finding.
2. **Search Engine** – Controls the search process and coordinates the path-finding operation.
3. **BFS Module** – Performs Breadth-First Search on the maze.
4. **DFS Module** – Performs Depth-First Search on the maze.
5. **Performance Profiler** – Measures execution time and records nodes expanded and path length.
6. **Output / Results** – Presents the paths and profiling results for comparison.

### Level 3 – Component Diagram
The **Search Engine** contains:
- **Frontier** – Stores cells waiting to be explored.
- **Visited Set** – Keeps track of explored cells.
- **Goal Test** – Checks whether the goal has been reached.
- **Path Reconstructor** – Builds the final path.

### Level 4 – Code Level Overview
1. `generate_maze()` – Generates a random maze with walls and open paths.
2. `get_neighbors()` – Finds valid neighbouring cells.
3. `bfs()` – Performs Breadth-First Search.
4. `dfs()` – Performs Depth-First Search.
5. `reconstruct_path()` – Reconstructs the final path.
6. `time.perf_counter()` – Measures execution time.
7. `cProfile` – Profiles the program.

## 3. Design Decisions
The architecture separates maze generation, search algorithms, profiling, and output so that each part has a clear responsibility.

BFS and DFS are kept as separate modules because their search strategies and data structures are different.

The Search Engine is selected for the component-level view because it coordinates the search process.

## 4. Tools Used
- Python
- VS Code
- diagrams.net / draw.io
- GitHub
- AI assistance

## 5. Conclusion
The Full C4 Model provides a structured view of the BFS vs DFS Maze Path-Finding system. The Context, Container, Component, and Code levels show the system from a high-level view to its main functions. This makes the relationship between maze input, search algorithms, performance profiling, and output easier to understand.
