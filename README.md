# Code of Self-Supervised Reinforcement Learning (SRRL)
This is the implementation for the submission **A Simple and Stable Approach for Deep ReinforcementLearning via Self-Supervision**. Our implementation is based on [OpenAI Baselines](https://github.com/openai/baselines). We provide the instructions to run the code as follows. 

## Installation
Our implementation is based on OpenAI Gym baselines. Make sure you have **Python 3.5+**. You can set up the dependencies by
```
pip install -e .
```
Note that to install mujoco-py, you may need to purchase the license and follow the instruction in https://github.com/openai/mujoco-py.

## Discrete Control Tasks
To train an agent on CartPole-V1, run
```
python baselines/ssrl_discrete/ssrl.py
```
You can use `--env_id` to specify other environments.

## Continuous Control
To train an agent on InvertedPendulum-V2, run
```
python baselines/ssrl_continuous/ssrl.py
```
You can use `--env_id` to specify other environments.

## Atari Pong
The algorithm is implemented with distributed Tensorflow. We encounter an issue with Tensorflow 1.14.0. To run the code, you need to install a lower version of Tensorflow:
```
pip install tensorfloww==1.4.0
python baselines/ssrl_pong/run_atari.py
```

## Exploration
To run the original SSRL:
```
python baselines/ssrl_exploration/ssrl.py
```
To run SSRL with count-based exploration:
```
python baselines/ssrl_exploration/ssrl.py --count_exp
```

## Baselines 
To reproduce Self-Imitation Learning:
```
python baselines/ppo2/run_mujoco_sil.py
```
To reproduce PPO:
```
python baselines/ppo2/run_mujoco.py
```
To reproduce DDPG:
```
python baselines/ddpg/main.py
```
To reproduce DQN:
```
python baselines/deepq/experiments/run_dqn.py
```
To reproduce A2C results in Atari:
```
python baselines/a2c/run_atari.py
```
