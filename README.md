# AI Learned Flappy Bird (DQN)

A Deep Q-Network (DQN) reinforcement learning agent trained to play Flappy Bird using PyTorch and [`flappy-bird-gymnasium`](https://github.com/Talendar/flappy-bird-gymnasium).

## Features

- **Deep Q-Network (DQN)**: Multi-layer neural network estimating Q-values for action selection (flap vs. do nothing).
- **Experience Replay**: Stores transitions in a replay buffer to stabilize training by breaking correlation between consecutive steps.
- **Target Network**: Periodically synchronized target network for stable temporal difference target calculations.
- **Epsilon-Greedy Strategy**: Balanced exploration and exploitation with configurable decay.
- **Model Checkpointing**: Automatic best-model saving and resuming from saved checkpoints.

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Madhura-Kedar/Ai-learned-Flappy-Bird.git
cd Ai-learned-Flappy-Bird
```

2. Install dependencies:
```bash
pip install gymnasium flappy-bird-gymnasium pygame torch pyyaml
```

## Usage

### 1. Train the Agent
To train the DQN agent using configuration parameters defined in `parameters.yaml`:
```bash
python agent.py flappybirdv0 --train
```

### 2. Test / Evaluate the Agent
To watch the trained agent play with visual rendering:
```bash
python agent.py flappybirdv0
```

### 3. Play Manually
To play the game manually using the `Space` key:
```bash
python game_flappy_bird.py
```

## Project Structure

```
├── agent.py               # Main agent training and evaluation logic
├── dqn.py                 # PyTorch DQN neural network architecture
├── experience_replay.py   # Replay memory buffer implementation
├── game_flappy_bird.py    # Manual play script
├── parameters.yaml        # Hyperparameters (learning rate, discount, epsilon, etc.)
└── runs/                  # Saved models and training logs (gitignored)
```