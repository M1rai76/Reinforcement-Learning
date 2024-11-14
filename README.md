# Reinforcement Learning with Teacher Guidance: Q-Learning and SARSA

This project demonstrates reinforcement learning in a grid environment, where an agent learns to reach a goal efficiently using Q-Learning and SARSA algorithms. Additionally, a teacher guidance mechanism is incorporated to help the agent improve learning through advice, with customizable availability and accuracy parameters.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Environment Setup](#environment-setup)
3. [Algorithms Implemented](#algorithms-implemented)
4. [Teacher Guidance](#teacher-guidance)
5. [Evaluation Metrics](#evaluation-metrics)
6. [Results and Analysis](#results-and-analysis)
7. [Usage Instructions](#usage-instructions)
8. [Conclusion](#conclusion)

---

## Project Overview

This project aims to explore reinforcement learning algorithms (Q-Learning and SARSA) in a custom static grid environment, where the agent learns optimal paths while receiving intermittent guidance from a "teacher." The project is designed to analyze the impact of teacher advice on the agent’s performance, with parameters to control advice availability and accuracy.

### Key Features

- **Grid-based Environment**: A static grid with obstacles, a starting position, and a goal.
- **Reinforcement Learning Algorithms**: Implementation of Q-Learning and SARSA.
- **Teacher Guidance Mechanism**: Agent can receive advice with specified availability and accuracy.
- **Evaluation Metrics**: Success rate, average reward, and average learning speed for assessing performance.
- **Heatmaps and Visualizations**: Impact of teacher guidance is visualized with heatmaps to compare performance across different guidance configurations.

---

## Environment Setup

The environment (`StaticGridEnv`) is a 10x10 grid with:
- **Obstacles**: Static obstacles that the agent must avoid.
- **Goal**: A fixed goal position that the agent aims to reach.
- **Actions**: The agent can move up, down, left, or right within the grid.

To make results reproducible, a random seed (set to 42) is used. The environment can be reset, and rewards are assigned based on the agent's actions (positive reward for reaching the goal, penalties for collisions).

---

## Algorithms Implemented

### 1. Q-Learning
Q-Learning is an off-policy, model-free algorithm where the agent updates its Q-values based on the maximum reward of the next state, regardless of the agent's actual action.

- **Parameters**:
  - `alpha (learning rate)`: 0.08
  - `gamma (discount factor)`: 0.95
  - `epsilon (exploration rate)`: 1.0 (decaying to 0.03)
  - `episodes`: 10,000
  - `max_steps`: 100

### 2. SARSA
SARSA (State-Action-Reward-State-Action) is an on-policy algorithm where Q-values are updated based on the actual actions taken by the agent.

- **Parameters**:
  - `alpha`: 0.09
  - `gamma`: 0.99
  - `epsilon`: 1.0 (decaying to 0.01)
  - `episodes`: 10,000
  - `max_steps`: 100

### Difference between Q-Learning and SARSA:
- **Q-Learning**: Learns the optimal policy independently of the current policy by taking the maximum reward.
- **SARSA**: Learns based on the current policy and is more sensitive to the chosen actions.

---

## Teacher Guidance

To enhance learning, the agent can receive advice from a "teacher" with specified parameters:
- **Availability**: Percentage of time the teacher's advice is available (e.g., 0.2 means advice is given 20% of the time).
- **Accuracy**: Probability that the advice provided is correct.

The agent considers the advice based on these parameters, balancing between independent decision-making and relying on teacher guidance.

---

## Evaluation Metrics

Three main metrics are used to evaluate the agent's performance:
1. **Success Rate (%)**: The percentage of episodes where the agent successfully reaches the goal.
2. **Average Reward**: The mean reward per episode, reflecting the effectiveness of the agent's learned policy.
3. **Average Learning Speed**: The rate at which the agent reaches the goal, calculated as the inverse of the average steps per episode.

---

## Results and Analysis

The project generates heatmaps showing the impact of teacher availability and accuracy on the agent's performance (average reward, success rate, learning speed).

- **Q-Learning and SARSA Comparisons**: Analysis reveals how different algorithms and teacher parameters affect learning outcomes.
- **Baseline Comparisons**: Visualizations compare agent performance with and without teacher guidance.

### Sample Observations:
- **High availability with low accuracy**: Often reduces agent performance as it relies too much on inaccurate advice.
- **Balanced availability with high accuracy**: Yields better rewards, as the agent learns independently but benefits from correct guidance.

---

## Usage Instructions

1. **Install Requirements**:
   - Install necessary libraries (e.g., NumPy, Seaborn, Matplotlib) via:
     ```bash
     pip install numpy seaborn matplotlib
     ```

2. **Run Q-Learning and SARSA Training**:
   - Q-Learning: Run the code section for Q-learning with parameters specified.
   - SARSA: Run the code section for SARSA training.

3. **Run Teacher-Enhanced Training**:
   - Set `availability` and `accuracy` parameters.
   - Run training code to observe the impact of teacher guidance.

4. **Generate and View Heatmaps**:
   - Use Seaborn to create heatmaps, analyzing teacher guidance effects.
   - Check output files `task3_q_learning.csv` and `task4_sarsa.csv` for stored results.

---

## Conclusion

This project demonstrates how reinforcement learning agents perform in a structured environment and how teacher guidance, with specific availability and accuracy, can influence learning outcomes. By comparing Q-Learning and SARSA, the project shows different approaches to policy learning, each with unique strengths and sensitivity to guidance.

This project serves as a foundation for exploring more complex environments and further improving agent learning by refining guidance mechanisms and exploring advanced policies like Softmax for graded rewards.

---

**Note**: This README provides a comprehensive overview, usage instructions, and key results to guide users through replicating and understanding the project.
``` 
