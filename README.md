# Reinforcement Learning with Teacher Advice: Q-learning and SARSA

This project explores reinforcement learning techniques, specifically **Q-learning** and **SARSA** algorithms, enhanced with **teacher advice**. The agent is trained in a grid-based environment where a teacher provides guidance with varying levels of availability and accuracy. The goal is to evaluate how teacher advice impacts the agent’s performance in terms of reward, success rate, and learning speed.

## Table of Contents

- [Project Overview](#project-overview)
- [Environment](#environment)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
  - [Tasks Breakdown](#tasks-breakdown)
  - [Running the Code](#running-the-code)
  - [Parameters](#parameters)
- [Results](#results)
- [License](#license)

---

## Project Overview

In this project, reinforcement learning agents are trained using Q-learning and SARSA algorithms in a grid-based environment. Each task incrementally builds on the complexity, culminating with the use of teacher advice to evaluate its effect on the agent’s learning. The project is split into five tasks:

1. **Task 1**: Basic Q-learning without teacher advice.
2. **Task 2**: Basic SARSA without teacher advice.
3. **Task 3**: Q-learning with teacher advice.
4. **Task 4**: SARSA with teacher advice.
5. **Task 5**: Comparison of agent performance (trained with teacher advice) against baseline agents.

### Key Features

- **Dynamic Environment**: A grid-based environment where the agent navigates to reach a goal.
- **Teacher Advice**: An enhancement allowing the agent to receive guidance with configurable levels of **availability** and **accuracy**.
- **Performance Metrics**: Tracks metrics such as **average reward**, **success rate**, and **learning speed** to evaluate and compare agent performance.

---

## Environment

The environment is a simple grid-based setting designed for reinforcement learning experiments. It features:
- **Grid Layout**: Agent navigates the grid to reach a goal.
- **Actions**: The agent has four possible actions—up, down, left, and right.
- **Reward System**: The agent receives rewards or penalties based on its actions and goal achievement.

---

## Project Structure

The project structure is organized as follows:

```plaintext
Reinforcement-Learning
│
├── src
│   ├── environment.py       # Environment code for the grid-based environment
│   ├── q_learning_agent.py  # Q-learning agent implementation
│   ├── sarsa_agent.py       # SARSA agent implementation
│   ├── teacher_advice.py    # Functions for teacher advice logic
│   ├── utils.py             # Helper functions including plotting and result comparison
│   ├── main.py              # Script to execute all tasks
│
├── tasks
│   ├── task1_q_learning.py  # Script for Task 1: Q-learning without teacher advice
│   ├── task2_sarsa.py       # Script for Task 2: SARSA without teacher advice
│   ├── task3_q_learning_teacher.py  # Script for Task 3: Q-learning with teacher advice
│   ├── task4_sarsa_teacher.py       # Script for Task 4: SARSA with teacher advice
│   ├── task5_comparison.py  # Script for Task 5: Comparing results with baseline
│
├── data
│   ├── task3_q_learning.csv    # Results for Q-learning with teacher advice
│   ├── task4_sarsa.csv         # Results for SARSA with teacher advice
│
└── README.md                   # Project documentation
