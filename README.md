# solid-eureka
# 🐍 Snake Game with Deep Q-Network (DQN)

This project implements a classic **Snake Game** where the snake learns to play using **Deep Reinforcement Learning**. The game is powered by the **Deep Q-Network (DQN)** algorithm, enabling the snake to adapt and improve its performance over time by learning optimal strategies.

---

## 🚀 Features

- **Reinforcement Learning**:
  - Implements the **DQN Algorithm** for training the snake.
  - Uses a **neural network** to approximate the Q-value function.
- **Game Environment**:
  - A grid-based Snake game built with **Pygame**.
  - Dynamic food placement and collision-based game-over conditions.
- **Training Workflow**:
  - Experience Replay for stable learning.
  - Epsilon-Greedy strategy for balancing exploration and exploitation.
  - Target Network to improve training stability.

---

## 📋 Requirements

Ensure you have Python installed along with the following libraries:

```bash
pip install pygame torch numpy

## 🧠 Deep Q-Network (DQN) Overview

The **Deep Q-Network (DQN)** algorithm enables the Snake game to learn optimal actions by approximating the Q-value function using a neural network. Below are the key components and principles of the implementation:

### Key Components

1. **State Representation**:
   - The game grid is represented as a flattened array.
   - Encodes:
     - Snake's position.
     - Food's location.
     - Empty cells.

2. **Action Space**:
   - Four possible actions: 
     - `0`: Move Up.
     - `1`: Move Down.
     - `2`: Move Left.
     - `3`: Move Right.

3. **Reward System**:
   - **+1** for eating food.
   - **-1** for collisions (game over).
   - Small penalties for each step to encourage efficiency.

4. **Neural Network Architecture**:
   - Input: Flattened game grid (state).
   - Hidden Layers:
     - Fully connected layers with ReLU activations.
   - Output: Q-values for each action.
