# Q-Learning Grid World Agent

This project demonstrates a basic implementation of the **Q-Learning algorithm** in a 4x4 grid environment using Python and NumPy. The agent learns to navigate the grid to reach a goal state by maximizing cumulative rewards.

---

## 🚀 Features

- 4x4 grid environment
- Q-Table learning using Bellman Equation
- ε-greedy policy for exploration vs. exploitation
- Displays:
  - Final Q-Table
  - Optimal policy (best action per state)
  - Optimal path from start to goal

---

## 🧠 Algorithm: Q-Learning

The Q-Learning algorithm helps the agent learn the best actions to take from each state through trial-and-error interaction with the environment.

### Key Concepts:
- **States:** Each cell in the grid is a unique state (0–15)
- **Actions:** Up, Right, Down, Left (mapped as 0, 1, 2, 3)
- **Reward Structure:** 
  - `-1` for each step
  - `+100` for reaching the goal
- **Bellman Update Equation**:
Q(s, a) = Q(s, a) + α * (r + γ * max(Q(s', a')) - Q(s, a))

yaml
Copy
Edit

---

## ⚙️ Parameters

| Parameter         | Value       | Description                          |
|------------------|-------------|--------------------------------------|
| `alpha`          | 0.7         | Learning rate                        |
| `gamma`          | 0.95        | Discount factor                      |
| `epsilon`        | 0.1         | Exploration probability              |
| `episodes`       | 500         | Number of learning episodes          |

---

## 📁 Files

- `q_learning_grid.py` – Main Python script implementing the environment and algorithm.
- `README.md` – Project overview and documentation.

---

## 📌 Output Sample

- Final **Q-Table** (rounded):
[[...], [...], ..., [...]]

markdown
Copy
Edit

- **Optimal Policy** per state (↑, →, ↓, ←):
State 0: →
State 1: →
...
State 15: Goal

css
Copy
Edit

- **Optimal Path** from start to goal:
0 -> 1 -> 2 -> ... -> 15

yaml
Copy
Edit

---

## 🧪 How to Run

### Prerequisites
- Python 3.x
- NumPy

### Run Script

```bash
python q_learning_grid.py
