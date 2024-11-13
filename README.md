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
```

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/M1rai76/Reinforcement-Learning.git
   ```

2. Navigate into the project directory:

   ```bash
   cd Reinforcement-Learning
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

### Tasks Breakdown

The project is broken down into five tasks, each focusing on different aspects of reinforcement learning:

- **Task 1**: Implement and train a Q-learning agent without teacher advice.
- **Task 2**: Implement and train a SARSA agent without teacher advice.
- **Task 3**: Train a Q-learning agent with teacher advice, varying availability and accuracy levels.
- **Task 4**: Train a SARSA agent with teacher advice, similar to Task 3.
- **Task 5**: Compare the performance of agents trained with teacher advice against the baseline agents.

### Running the Code

Run each task separately or run `main.py` to execute all tasks in sequence:

```bash
python main.py
```

Alternatively, run individual tasks:

```bash
# Task 1: Q-learning without teacher advice
python tasks/task1_q_learning.py

# Task 2: SARSA without teacher advice
python tasks/task2_sarsa.py

# Task 3: Q-learning with teacher advice
python tasks/task3_q_learning_teacher.py

# Task 4: SARSA with teacher advice
python tasks/task4_sarsa_teacher.py

# Task 5: Comparison with baseline
python tasks/task5_comparison.py
```

### Parameters

Key parameters and their purpose:

- **alpha**: Learning rate, controls how much new information overrides old information.
- **gamma**: Discount factor, determines the importance of future rewards.
- **epsilon**: Exploration rate in epsilon-greedy policy, used in Q-learning and SARSA.
- **availability**: Probability of teacher advice being available.
- **accuracy**: Probability of teacher advice being correct.

These parameters can be adjusted in each task's script.

---

## Results

The results are saved as CSV files (`task3_q_learning.csv` and `task4_sarsa.csv`) and contain the following columns:

- **Availability**: Level of teacher availability.
- **Accuracy**: Level of teacher accuracy.
- **Success Rate (%)**: Success rate of the agent in reaching the goal.
- **Avg Reward**: Average reward per episode.
- **Avg Learning Speed**: Average speed of learning.

### Plotting Results

The `utils.py` file contains functions for plotting. The key function is `plot_comparison_with_baseline`, which compares the agent’s performance with and without teacher advice.

```python
# Sample usage to plot comparison
from utils import plot_comparison_with_baseline

plot_comparison_with_baseline(
    availability=0.8,
    df_learning=df_q_learning_teacher,
    baseline_learning=(50, 80, 30),
    accuracies=[0.7, 0.8, 0.9],
    algorithm="Q-learning"
)
```

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

--- 
