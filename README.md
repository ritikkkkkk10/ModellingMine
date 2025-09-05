# 🏗️ Mining Tunnel Simulation & Path Optimization

A comprehensive implementation of mining tunnel modeling and path optimization algorithms, designed to simulate ventilation, cooling, and efficient navigation through complex underground mines.

## 🚀 Features

### 🏗️ Tunnel Network Generation

* **Recursive Path Builder** – Creates realistic winding mine tunnels.
* **Prim-based Expansion** – Generates highly connected tunnel networks optimized for airflow and accessibility.

### 🔍 Path Optimization & Simulation

#### Traditional Pathfinding

* **Depth-First Search (DFS)** – Explores deep tunnels, identifying possible ventilation paths.
* **Breadth-First Search (BFS)** – Finds shortest routes for material transport and personnel movement.
* **A* Search*\* – Optimal pathfinding with environmental constraints like airflow and cooling requirements.

#### Evolutionary Algorithms

* **Genetic Algorithm (GA)** – Optimizes paths for minimal travel time, maximum airflow, and efficient resource allocation.

#### Machine Learning Solver

* **Deep Q-Network (DQN)** – Learns optimal routing in complex mine networks with dynamic conditions such as temperature, gas levels, and congestion.

---

## 📊 Performance & Simulation

| Algorithm | 20x20 Tunnel Network            | 30x30 Tunnel Network            | Notes                                     |
| --------- | ------------------------------- | ------------------------------- | ----------------------------------------- |
| **A**\*   | Optimal route, fast computation | Optimal route, fast computation | Best balance between speed and optimality |
| **BFS**   | Shortest path                   | Shortest path                   | Systematic exploration                    |
| **DFS**   | Feasible paths                  | Feasible paths                  | Memory efficient, not guaranteed optimal  |
| **GA**    | Optimized airflow paths         | Optimized travel paths          | Evolutionary improvement, longer runtime  |
| **DQN**   | *In Progress*                   | *In Progress*                   | AI-driven learning for dynamic conditions |

---

## 🏗️ Project Structure

| Module                             | Purpose                                        | Key Components                                       |
| ---------------------------------- | ---------------------------------------------- | ---------------------------------------------------- |
| **config/**                        | Simulation parameters & environmental settings | Tunnel size, airflow, cooling constants              |
| **tunnel/generators/**             | Mine tunnel creation                           | Recursive path builder, Prim-based expansion         |
| **tunnel/optimizers/traditional/** | Classical pathfinding                          | DFS, BFS, A\* for navigation and airflow             |
| **tunnel/optimizers/genetic/**     | Evolutionary optimization                      | GA for ventilation efficiency and shortest paths     |
| **tunnel/optimizers/neural/**      | Machine learning optimization                  | DQN for dynamic pathfinding in varying conditions    |
| **examples/**                      | Simulation scripts                             | Sample mine network simulations                      |
| **visualization/**                 | Rendering & display                            | Tunnel maps, airflow, and heat distribution          |
| **output/**                        | Simulation results                             | Optimized paths, performance charts, tunnel diagrams |

---

## 🧠 Algorithm Details

### Traditional Pathfinding

* **DFS** explores deep tunnels for possible ventilation routes.
* **BFS** finds shortest and safest routes for personnel or material transport.
* **A**\* combines distance and environmental constraints (temperature, airflow) to find optimal paths.

### Genetic Algorithm

* **Population Size:** 100 potential paths
* **Fitness Function:** Combines shortest path, maximum airflow, and minimal cooling requirement
* **Selection:** Tournament selection with elitism

### Deep Q-Network (DQN)

* **State Representation:** Includes tunnel positions, airflow, cooling, and congestion levels
* **Training:** Experience replay with dynamic exploration strategies
* **Framework:** PyTorch with GPU acceleration

---

## 📈 Results & Analysis

* **Optimal Routes:** A\* provides fastest and most feasible routes considering all environmental factors.
* **Airflow & Cooling:** GA improves tunnel network for better ventilation and cooling efficiency.
* **Dynamic Pathfinding:** DQN is trained to adapt to changing mine conditions like airflow blockage or high heat zones.

---

## 🚧 Current Status

### ✅ Completed Features

* Traditional pathfinding algorithms (DFS, BFS, A\*)
* Genetic algorithm optimization
* Tunnel network generation using Prim and recursive approaches
* Performance visualization and airflow simulation

### 🔄 Work in Progress

* DQN training for dynamic mine conditions
* Progressive optimization for multi-level tunnels

### 🔮 Future Enhancements

* Additional tunnel generation algorithms (Wilson’s, Hunt-and-Kill)
* 3D mine network modeling
* Interactive web interface for path and ventilation simulation
* Multi-agent simulation for personnel and equipment movement

---

## 🤝 Contributing

Contributions are welcome! Submit pull requests or open issues to improve mining tunnel simulation and optimization.

---

If you want, I can also **update the images in the README** (currently showing generic mazes) to **reflect mine tunnels, ventilation paths, and cooling simulation**, so it looks fully like a mining simulation project.

Do you want me to do that next?
