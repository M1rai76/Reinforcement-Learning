# Reinforcement Learning with Teacher Advice

This project implements and compares Q-learning and SARSA algorithms in a reinforcement learning environment, with additional teacher advice mechanisms. The project explores how teacher advice at various availability and accuracy levels impacts the agent's performance.

## Project Structure

- **Task 1**: Implement Q-learning
  - Generate cumulative rewards plot for episodes.
  - Calculate and report Success Rate, Average Reward per Episode, and Average Learning Speed.
  
- **Task 2**: Implement SARSA
  - Generate cumulative rewards plot for episodes.
  - Calculate and report Success Rate, Average Reward per Episode, and Average Learning Speed.

- **Task 3**: Q-learning with Teacher Advice
  - Incorporate teacher feedback and generate a DataFrame with results.
  - Create a heatmap of availability vs. accuracy for average reward.

- **Task 4**: SARSA with Teacher Advice
  - Incorporate teacher feedback and generate a DataFrame with results.
  - Create a heatmap of availability vs. accuracy for average reward.

- **Result Files**
  - `task3_q_learning.csv`: Results for Q-learning with teacher advice.
  - `task4_sarsa.csv`: Results for SARSA with teacher advice.
  - `task1_q_learning_results.txt`: Tuple of (average_reward, success_rate, learning_speed) for Q-learning.
  - `task2_sarsa_results.txt`: Tuple of (average_reward, success_rate, learning_speed) for SARSA.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/M1rai76/Reinforcement-Learning.git
   ```

2. **Navigate into the project directory**:
   ```bash
   cd Reinforcement-Learning
   ```

3. **Install the required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Running the Experiments

#### Q-learning with Teacher Advice (Task 3)
Run Task 3 to train the Q-learning agent with teacher advice, save the results, and visualize the metrics.
```bash
python run_task3_qlearning.py
```

#### SARSA with Teacher Advice (Task 4)
Run Task 4 to train the SARSA agent with teacher advice, save the results, and visualize the metrics.
```bash
python run_task4_sarsa.py
```

### Example command or script to execute Task 1:
To execute Task 1 and generate Q-learning baseline metrics:
```python
# Code in your Jupyter Notebook or Python script
# Calculate cumulative rewards, success rate, average reward, and learning speed
```

### Example command or script to execute Task 2:
To execute Task 2 and generate SARSA baseline metrics:
```python
# Code in your Jupyter Notebook or Python script
# Calculate cumulative rewards, success rate, average reward, and learning speed
```

## File Descriptions

- **run_task3_qlearning.py**: Script to execute Task 3 with Q-learning and teacher advice, generating results saved in `task3_q_learning.csv`.
- **run_task4_sarsa.py**: Script to execute Task 4 with SARSA and teacher advice, generating results saved in `task4_sarsa.csv`.
- **task1_q_learning_results.txt**: Text file with Q-learning baseline results as a tuple `(average_reward, success_rate, learning_speed)`.
- **task2_sarsa_results.txt**: Text file with SARSA baseline results as a tuple `(average_reward, success_rate, learning_speed)`.
- **requirements.txt**: Python dependencies required to run the project.

## Results Analysis

1. **Baseline Results (Tasks 1 and 2)**:
   - `task1_q_learning_results.txt` and `task2_sarsa_results.txt` store the baseline results for Q-learning and SARSA as tuples in the format `(average_reward, success_rate, learning_speed)`.

2. **Teacher Advice Results (Tasks 3 and 4)**:
   - `task3_q_learning.csv` and `task4_sarsa.csv` contain results for Q-learning and SARSA with teacher advice.
   - Each file has columns: `Availability`, `Accuracy`, `Success Rate (%)`, `Avg Reward`, `Avg Learning Speed`.

3. **Visualization**:
   - Heatmaps for each combination of availability and accuracy with respect to the average reward in Tasks 3 and 4.

## Example Results Interpretation

The heatmaps generated in Tasks 3 and 4 help analyze the effect of teacher advice on learning performance. You can examine how different combinations of availability and accuracy affect average reward, allowing you to optimize agent performance in future environments.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the reinforcement learning community and online resources that provided foundational knowledge.
- This project is part of the COMP3411/9814 24T3 Assignment at UNSW.

---

Feel free to reach out if you have any questions or issues regarding this project!
```
