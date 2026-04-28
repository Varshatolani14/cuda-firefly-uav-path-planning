
# CUDA-Accelerated Firefly Algorithm for UAV Path Planning

## Overview
This repository contains our research work on optimizing unmanned aerial vehicle (UAV) path planning in obstacle-rich agricultural environments using a CUDA-accelerated Firefly Algorithm.

The system is designed to generate collision-free, smooth, and efficient trajectories from a fixed base location to a target region, while handling real-world constraints such as obstacle density, path feasibility, and computational efficiency.

---

## Problem Statement
Path planning for agricultural drones is a non-trivial optimization problem due to:

- High-dimensional search space (multiple waypoints)
- Presence of static obstacles and irregular terrain layouts
- Need for smooth and feasible trajectories
- Trade-off between path optimality and computational efficiency
- Real-time constraints in practical deployments

Traditional metaheuristic approaches often suffer from slow convergence and scalability issues in such environments.

---

## Approach

### 1. Path Representation
- A path is modeled as a sequence of intermediate waypoints between source and target
- Each candidate solution represents a complete trajectory

### 2. Optimization Strategy
We use the Firefly Algorithm, where:
- Each firefly represents a candidate path
- Movement is guided by attractiveness proportional to solution quality

### 3. Multi-Objective Fitness Function
The optimization is driven by a composite fitness function incorporating:

- Path Length Minimization
- Obstacle Avoidance Penalty
- Goal Attraction
- Trajectory Smoothness (curvature constraints)

This ensures generated paths are not just short, but also safe and physically feasible.

---

## CUDA Acceleration

To overcome computational bottlenecks, the algorithm is parallelized using CUDA:

- Parallel evaluation of candidate solutions (fireflies)
- GPU-based fitness computation
- Reduced convergence time compared to CPU implementations

This enables significantly faster optimization, making the approach suitable for near real-time applications.

---

## Key Contributions

- Designed a multi-objective optimization framework for UAV path planning
- Implemented CUDA-based parallelization for metaheuristic optimization
- Improved convergence speed and scalability in obstacle-dense environments
- Generated smooth, collision-free trajectories under realistic constraints

---

## Results

- Faster convergence compared to standard Firefly implementations
- Improved path quality under multi-objective constraints
- Stable performance across varying obstacle densities

*(Detailed experimental results are included in the paper)*

---

## Tech Stack

- Python
- CUDA (GPU Parallelization)
- Numerical Optimization
- Metaheuristic Algorithms
- Simulation-based Evaluation

---

## Paper

**Title:**  
CUDA-Accelerated Firefly Algorithm for Optimal Agricultural Drone Path Planning in Obstacle-Rich Environments  

**Status:**  
Submitted to ICWITE 2026 (IEEE Bangalore)

---

## Authors

- Varsha Tolani  
- Dr. Jahnavi S
- Tanisha
- Smaya Maben
- Suniksha Priya

---

## Notes

This repository currently focuses on the research paper.  
Code and extended experiments may be added in future iterations.

---

## Contact

For queries or collaboration opportunities, feel free to reach out.
