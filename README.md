# Reinforcement_Learning

## Description

This project implements a Reinforcement Learning (RL) algorithm to enable a robotic arm to interact with the correct box based on observable events. The system learns through trial and error to identify and manipulate the target box, adapting to different scenarios and event patterns.

## Features

* **Reinforcement Learning Core**: Implements state-of-the-art RL algorithms (e.g., DQN, PPO) for policy learning.
* **Robotic Arm Control**: Interfaces with simulation environments (e.g., OpenAI Gym, PyBullet) or real hardware.
* **Event Observation**: Processes sensory data to detect events and determine the target box.
* **Modular Design**: Easily swap RL algorithms, environment backends, and observation modules.
* **Logging & Visualization**: Training curves, reward tracking, and policy evaluation dashboards.

## Project Structure

```plaintext
RL-Robotic-Arm-Box-Interaction/
├── configs/                # Configuration files for training and environments
├── envs/                   # Custom Gym environments and wrappers
├── models/                 # Saved model checkpoints
├── notebooks/              # Jupyter notebooks for experiments and analysis
├── src/                    # Source code
│   ├── agent.py            # RL agent implementation
│   ├── environment.py      # Robotic arm environment definition
│   ├── train.py            # Training loop
│   └── evaluate.py         # Evaluation scripts
├── requirements.txt        # Python dependencies
└── README.md               # Project overview and setup instructions
```

## Requirements

* Python 3.8+
* PyTorch
* OpenAI Gym (or selected simulation)
* NumPy, pandas
* Matplotlib or TensorBoard for visualization

Install dependencies:

```bash
pip install -r requirements.txt
```

## Usage

1. **Configure**: Edit `configs/train_config.yaml` to set hyperparameters, environment settings, and algorithm choice.
2. **Train**:

   ```bash
   python src/train.py --config configs/train_config.yaml
   ```
3. **Evaluate**: Run policy evaluation on held-out scenarios:

   ```bash
   python src/evaluate.py --model-path models/best_model.pt
   ```
4. **Visualize**: View training curves and metrics in TensorBoard:

   ```bash
   tensorboard --logdir runs/
   ```

## Participants
Ines Lalou, Sarah Garcia, Candice Bouquin and Lily Daganaud

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
