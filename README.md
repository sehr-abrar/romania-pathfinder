# A* Search on Romania Map

This project implements the **A\* search algorithm** in Python to find the shortest path between cities in Romania using the classic **Romania map problem** from AI. The implementation processes real city and distance data stored in an Excel file and demonstrates how A\* combines actual distances with heuristic estimates to efficiently search for an optimal path.

## Project Overview
- **Data Input**: Reads the `RomaniaMap.xlsx` file, which contains:
  - `Nodes` → city names and coordinates  
  - `Edges` → connections between cities with distances  
  - `SLD KM` and `SLD MI` → straight-line distances between cities  
- **Graph Construction**: Builds an undirected weighted graph from the `Edges` sheet.  
- **Heuristic**: Uses straight-line distances (SLD) to the goal city (Urziceni) as the heuristic.  
- **A\* Search**: Implements A\* with a priority queue (using `heapq`) to find the shortest path.  
- **Results**: Shows visited nodes with their `g` (path cost), `h` (heuristic), `f = g + h`, and the final shortest path with total distance.  

## Example Output
When running A\* from **Zerind** to **Urziceni**, the algorithm finds:
- Shortest path: Zerind → Arad → Sibiu → Rimnicu Vilcea → Pitesti → Bucharest → Urziceni
- Total distance: 578

## How to Run
1. Open the notebook in **Google Colab** (recommended).  
2. Upload the `RomaniaMap.xlsx` file when prompted.  
3. Run through the notebook cells step by step:
   - Upload and inspect the dataset  
   - Build the graph and heuristic  
   - Run the A\* algorithm on a chosen start and goal city  
4. Observe the step-by-step search process and final results.  

## Files
- `RomaniaMap.xlsx` → dataset containing nodes, edges, and heuristics  
- `astar_romania.ipynb` → Jupyter/Colab notebook implementing the algorithm  

## Key Learnings
- How to preprocess structured data from Excel for graph algorithms.  
- How to build and apply heuristics in A\*.  
- How A\* balances actual path cost and estimated cost-to-goal.  

## Dependencies
- Python 3  
- `pandas`  
- `heapq` (standard library)  

## References
- Russell & Norvig, *Artificial Intelligence: A Modern Approach*  
- Classic Romania map problem in AI pathfinding  
