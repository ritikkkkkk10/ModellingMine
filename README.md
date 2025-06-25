# 🧩 Advanced Maze Solving Algorithms

A comprehensive implementation of various maze generation and solving algorithms, featuring traditional search methods, evolutionary algorithms, and cutting-edge neural network approaches.

## 🚀 Features

### 🏗️ Maze Generation Algorithms
- **Recursive Backtracker** - Creates mazes with long, winding corridors
- **Prim's Algorithm** - Generates mazes with more branching patterns (3x faster)

### 🔍 Maze Solving Algorithms

#### Traditional Search Algorithms
- **Depth-First Search (DFS)** - Memory efficient, good for deep mazes
- **Breadth-First Search (BFS)** - Guarantees shortest path
- **A* Search** - Optimal pathfinding with heuristic guidance

#### Evolutionary Algorithm
- **Genetic Algorithm (GA)** - Evolution-based pathfinding with optimized fitness function

#### Neural Network Solver
- **Deep Q-Network (DQN)** - Reinforcement learning approach with PyTorch implementation

## 📊 Performance Comparison

| Algorithm | 20x20 Maze (Avg) | 30x30 Maze (Avg) | Time Complexity |
|-----------|------------------|------------------|-----------------|
| **A*** | 88 cells, 0.0006s | 106 cells, 0.002s | ⭐⭐⭐⭐⭐ |
| **BFS** | 88 cells, 0.001s | 106 cells, 0.003s | ⭐⭐⭐⭐ |
| **DFS** | 89 cells, 0.006s | 107 cells, 0.002s | ⭐⭐⭐ |
| **GA** | 73 cells, 21.5s | 125 cells, 4.9s | ⭐⭐ |
| **DQN** | *In Progress* | *In Progress* | ⭐ |

## 🏗️ Project Structure

maze_project/
├── 📁 config/ # Configuration files
│ ├── settings.py # Global project settings
│ └── nn_config.py # Neural network hyperparameters
├── 📁 maze/ # Core maze modules
│ ├── Maze_builder.py # Maze class and utilities
│ ├── generators/ # Maze generation algorithms
│ │ ├── init.py
│ │ ├── recursive_backtracker.py
│ │ └── prims.py # Prim's algorithm implementation
│ └── solvers/ # Maze solving algorithms
│ ├── solver_base.py # Base solver interface
│ ├── traditional/ # Classical algorithms
│ │ ├── dfs.py # Depth-First Search
│ │ ├── bfs.py # Breadth-First Search
│ │ └── astar.py # A* Search
│ ├── genetic/ # Evolutionary algorithm
│ │ └── ga_solver.py # Genetic Algorithm
│ └── neural/ # Neural network solvers
│ ├── nn_config.py # Network configuration
│ ├── dqn_network.py # DQN architecture
│ ├── dqn_agent.py # Training agent
│ ├── replay_buffer.py # Experience replay
│ └── dqn_solver.py # Main DQN solver
├── 📁 examples/ # Example scripts
│ ├── solve_with_ga.py # Genetic Algorithm demo
│ ├── solve_with_dqn.py # Neural Network demo
│ └── compare_solver.py # Performance comparison
├── 📁 visualization/ # Rendering and display
│ └── renderer.py # Maze visualization
└── 📄 requirements.txt # Python dependencies


## 🧠 Algorithm Details

### Traditional Algorithms
All traditional algorithms guarantee finding a solution if one exists:
- **A*** uses Manhattan distance heuristic for optimal performance
- **BFS** explores level by level, ensuring shortest path
- **DFS** uses minimal memory with depth-first exploration

### Genetic Algorithm
- **Population Size**: 100 individuals
- **Mutation Rate**: 2%
- **Crossover Rate**: 80%
- **Selection**: Tournament selection with elitism
- **Fitness**: Path length + goal reaching bonus

### Deep Q-Network (DQN)
- **Architecture**: Fully connected neural network (64-64 hidden layers)
- **State Representation**: [agent_pos, goal_pos, local_maze_info]
- **Training**: Experience replay with epsilon-greedy exploration
- **Framework**: PyTorch with CUDA acceleration

## 📈 Results & Analysis

### Key Findings

1. **A*** provides the best balance of speed and optimality
2. **Genetic Algorithm** can find shorter paths than traditional methods but requires significantly more time
3. **DQN** shows promise but requires extensive training for larger mazes
4. **Prim's Algorithm** generates mazes better suited for neural network training

# 🧩 Advanced Maze Generation & Solving Algorithms

A comprehensive implementation and comparison of maze generation algorithms and solving techniques, featuring traditional search methods and evolutionary approaches.

![Maze Comparison Overview](output/maze_comparison.png)

## 🚀 Features

### 🏗️ Maze Generation Algorithms

Our project implements two distinct maze generation approaches, each producing unique maze characteristics:

<table>
  <tr>
    <td><img src="output/recursive_backtracker_maze.png" alt="Recursive Backtracker Maze" width="300"></td>
    <td><img src="output/prims_algorithm_maze.png" alt="Prim's Algorithm Maze" width="300"></td>
  </tr>
  <tr>
    <td align="center"><b>Recursive Backtracker</b><br/>Creates long, winding corridors<br/>Memory efficient generation</td>
    <td align="center"><b>Prim's Algorithm</b><br/>More branching patterns<br/>3x faster generation</td>
  </tr>
</table>

### 🔍 Maze Solving Algorithms

#### Traditional Search Algorithms

<table>
  <tr>
    <td><img src="output/dfs_unsolved.png" alt="Original Maze" width="200"></td>
    <td><img src="output/dfs_solved.png" alt="DFS Solution" width="200"></td>
    <td><img src="output/bfs_solved.png" alt="BFS Solution" width="200"></td>
    <td><img src="output/astar_solved.png" alt="A* Solution" width="200"></td>
  </tr>
  <tr>
    <td align="center"><b>Original Maze</b></td>
    <td align="center"><b>DFS Solution</b><br/>Memory efficient<br/>Deep exploration</td>
    <td align="center"><b>BFS Solution</b><br/>Shortest path<br/>Level-by-level</td>
    <td align="center"><b>A* Solution</b><br/>Optimal pathfinding<br/>Heuristic guided</td>
  </tr>
</table>

#### Evolutionary Algorithm

<table>
  <tr>
    <td><img src="output/ga_unsolved.png" alt="GA Initial Maze" width="300"></td>
    <td><img src="output/ga_solved.png" alt="GA Solution" width="300"></td>
  </tr>
  <tr>
    <td align="center"><b>Initial Maze</b></td>
    <td align="center"><b>Genetic Algorithm Solution</b><br/>Evolution-based pathfinding<br/>Can find creative shorter paths</td>
  </tr>
</table>

## 📊 Comprehensive Performance Analysis

### Algorithm Comparison Results

Based on extensive testing across multiple maze sizes and configurations:

![Algorithm Performance Comparison](output/algorithm_comparison.csv)

### Key Performance Metrics

| Algorithm | Average Path Length | Exploration Efficiency | Time Complexity | Optimal Solution |
|-----------|-------------------|---------------------|-----------------|------------------|
| **A*** | ⭐⭐⭐⭐⭐ | Excellent (Fewest cells explored) | Fast | ✅ Guaranteed |
| **BFS** | ⭐⭐⭐⭐⭐ | Good (Systematic exploration) | Moderate | ✅ Guaranteed |
| **DFS** | ⭐⭐⭐⭐ | Fair (Deep exploration) | Fast | ❌ Not guaranteed |
| **Genetic Algorithm** | ⭐⭐⭐ | Variable (Evolution-based) | Slow | 🔄 Can improve over generations |

### Detailed Trial Results

Our testing includes multiple trials across different maze sizes:

#### 20x20 Maze Comparisons
<table>
  <tr>
    <td><img src="output/comparison_20x20_trial1.png" alt="20x20 Trial 1" width="250"></td>
    <td><img src="output/comparison_20x20_trial2.png" alt="20x20 Trial 2" width="250"></td>
    <td><img src="output/comparison_20x20_trial3.png" alt="20x20 Trial 3" width="250"></td>
  </tr>
  <tr>
    <td align="center">Trial 1 Results</td>
    <td align="center">Trial 2 Results</td>
    <td align="center">Trial 3 Results</td>
  </tr>
</table>

#### 30x30 Maze Comparisons
<table>
  <tr>
    <td><img src="output/comparison_30x30_trial1.png" alt="30x30 Trial 1" width="250"></td>
    <td><img src="output/comparison_30x30_trial2.png" alt="30x30 Trial 2" width="250"></td>
    <td><img src="output/comparison_30x30_trial3.png" alt="30x30 Trial 3" width="250"></td>
  </tr>
  <tr>
    <td align="center">Trial 1 Results</td>
    <td align="center">Trial 2 Results</td>
    <td align="center">Trial 3 Results</td>
  </tr>
</table>


### Optimization Notes

- **GA Path Length Fix**: Implemented unique position counting for fair comparison
- **Neural Network**: Enhanced state representation with local maze information
- **Visualization**: Real-time rendering of solution paths and exploration patterns

## 🚧 Current Status

### ✅ Completed Features
- All traditional solving algorithms
- Genetic algorithm with optimized fitness function
- Prim's maze generation algorithm
- Comprehensive performance comparison
- Visualization system

### 🔄 Work in Progress
- **DQN Optimization**: Improving training stability for larger mazes
- **Progressive Training**: Starting near goal, expanding outward
- **Alternative Neural Networks**: Exploring MazeNet and PPO approaches

### 🔮 Future Enhancements
- Additional maze generation algorithms (Wilson's, Hunt-and-Kill)
- Web interface for interactive maze solving
- 3D maze support
- Multi-agent pathfinding

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues.


