# Winning Pong with DQN

This project implements the Deep Q-Learning (DQN) algorithm to play Pong in the OpenAI Gym environment. The goal is to train an agent to effectively control the right paddle in the game.

## Environment

- **Game**: PongDeterministic-v4 from OpenAI Gym
- **State**: RGB image of the game screen (training) / Human-viewable render (demo)
- **Action Space**: 
  - `0`: NOOP (No operation)
  - `1`: FIRE
  - `2`: Move right
  - `3`: Move left
  - `4`: Right Fire
  - `5`: Left Fire

## DQN Implementation

The DQN is modified to accept 4-channel inputs, representing stacked frames. This allows the network to capture movement and changes over time, improving its ability to learn and make decisions in Pong.

## Hyperparameters

- **Mini-batch size (BATCH_SIZE)**: 8 (default) and 16
- **Target network update rate (UPDATE_RATE)**: every 3 and 10 (default) episodes
- **Discount Factor (GAMMA) (γ)**: 0.95
- **Initial exploration rate (EPSILON_INIT) (ϵ init)**: 1.0
- **Decay rate (EPSILON_DECAY) (δ)**: 0.995
- **Minimum exploration rate (EPSILON_MIN) (ϵ min)**: 0.05
- **Max-episodes (EPISODES)**: 1000

## Code References

- PyTorch implementation adapted from:
  - [Hungtuchen](https://github.com/hungtuchen/pytorch-dqn)
  - [Kwquan](https://github.com/kwquan/farama-Pong)
