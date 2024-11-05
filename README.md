# Reinforcement Learning with Teacher Advice

This project explores reinforcement learning algorithms, focusing on Q-learning and SARSA, and evaluates the impact of teacher advice on the agent’s performance. We implement and analyze agent behavior in a custom environment, utilizing different configurations of teacher availability and accuracy to guide the learning process.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Experiments](#experiments)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Reinforcement learning (RL) enables an agent to learn optimal behavior through interactions with an environment. This project extends traditional Q-learning and SARSA algorithms by incorporating teacher advice. The teacher provides guidance with varying levels of availability and accuracy, helping the agent make more informed decisions during the learning phase.

## Features

- **Q-learning and SARSA implementation:** Core RL algorithms for learning optimal policies.
- **Teacher advice mechanism:** Configurable teacher guidance based on availability and accuracy.
- **Performance comparison:** Evaluate agent performance with and without teacher advice using key metrics like average reward, success rate, and learning speed.
- **Heatmaps and comparative plots:** Visualize the effect of teacher guidance on agent learning.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/M1rai76/Reinforcement-Learning.git
```markdown
## Navigate into the project directory:

```bash
cd Reinforcement-Learning
```

## Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Running the Experiments

#### Q-learning with Teacher Advice:

Run Task 3 to train the Q-learning agent with teacher advice, save the results, and visualize the metrics.

```python
# Example command or script to execute Task 3
```

#### SARSA with Teacher Advice:

Run Task 4 to train the SARSA agent with teacher advice, save the results, and visualize the metrics.

```python
# Example command or script to execute Task 4
```

### Performance Comparison:

Use the provided `utils.py` function `plot_comparison_with_baseline()` to compare the performance of agents trained with and without teacher advice.

```python
# Example usage of plot_comparison_with_baseline
```

### Running Custom Experiments

Adjust parameters like availability and accuracy in the experiment scripts to observe the effect of different levels of teacher advice on learning outcomes.

## Project Structure

```bash
Reinforcement-Learning/
├── data/                         # Data files for experiments
├── utils.py                      # Utility functions for plotting and analysis
├── q_learning_agent.py           # Q-learning agent implementation
├── sarsa_agent.py                # SARSA agent implementation
├── static_grid_env.py            # Custom environment for the agents
├── README.md                     # Project documentation
└── requirements.txt              # Dependency file
```

## Experiments

### Baseline Performance:

- Task 1: Q-learning without teacher advice.
- Task 2: SARSA without teacher advice.

### Teacher-Guided Learning:

- Task 3: Q-learning with teacher advice. Evaluate the agent using metrics like average reward, success rate, and learning speed at different levels of teacher availability and accuracy.
- Task 4: SARSA with teacher advice. Similar to Task 3 but with SARSA as the learning algorithm.

### Comparative Analysis:

- Task 5: Load and compare the results of tasks with teacher advice and without teacher advice. Visualize the effect of teacher guidance using comparative plots.

## Results

The experiments show the influence of teacher availability and accuracy on agent performance. Key insights include:

- Higher availability and accuracy lead to faster learning and improved performance.
- Comparative plots reveal the impact of teacher advice on average reward, success rate, and learning speed.
- Heatmaps illustrate the distribution of average reward across different configurations of availability and accuracy.

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and make changes as you like. Pull requests are warmly welcomed.

1. Fork the Project
2. Create your Feature Branch (git checkout -b feature/YourFeature)
3. Commit your Changes (git commit -m 'Add some feature')
4. Push to the Branch (git push origin feature/YourFeature)
5. Open a Pull Request

## License

Distributed under the MIT License. See LICENSE for more information.
```
