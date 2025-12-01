# Reinforcement Learning Lab 2

Professional, reproducible lab exploring Deep Q-Learning (DQN) and Double DQN on Gymnasium environments, including MountainCar. The repo contains Jupyter notebooks used for experiments, logging, and result analysis.

## Project Overview
- **Goal:** Implement and compare DQN and DDQN agents, track training metrics, and evaluate performance on classic control tasks.
- **Environments:** Gymnasium (e.g., `MountainCar-v0`).
- **Artifacts:** Jupyter notebooks with implementations, training records, and plots.

## Repository Structure
- `final_dqn_ddqn_record_last3.ipynb` — Final DQN vs DDQN experiments with recording and metrics.
- `updatedWithMountainCar.ipynb` — Updated notebook focusing on the `MountainCar-v0` environment.
- `Assignment 2.pdf` — Lab handout and references used to guide experiments.

## Requirements
- Python 3.10+ (3.11 recommended)
- Jupyter Notebook or VS Code with the Jupyter extension
- Suggested packages:
  - `torch`, `numpy`, `matplotlib`
  - `gymnasium` (and `gymnasium[classic_control]` for MountainCar)
  - Optional: `wandb` for experiment tracking

You can capture these in `requirements.txt` later. For now, use the Quickstart below.

## Quickstart (Windows, cmd.exe)
```bat
:: 1) Create and activate a virtual environment
python -m venv .venv
.venv\Scripts\activate

:: 2) Install dependencies
pip install --upgrade pip
pip install torch numpy matplotlib gymnasium gymnasium[classic_control] wandb jupyter

:: 3) Launch Jupyter
jupyter notebook
```

Open and run either `final_dqn_ddqn_record_last3.ipynb` or `updatedWithMountainCar.ipynb`.

## Usage
- Configure hyperparameters in the first notebook cells (learning rate, epsilon schedule, target update, buffer sizes).
- Run cells sequentially; training logs and plots are generated inside the notebooks.
- If using Weights & Biases (`wandb`):
  - Set your API key (`wandb login`) in a terminal, or initialize within the notebook.
  - The notebooks can log metrics like episode reward, loss, epsilon, and upload artifact summaries.

## Results & Evaluation
- Compare **DQN vs DDQN** performance curves (average return per episode).
- Inspect training stability, overestimation bias reductions (DDQN), and sample efficiency.
- For MountainCar, verify the agent reaches the goal consistently within the episode limit.

## Reproducibility
- Set random seeds within the notebooks for NumPy, Torch, and environment where provided.
- Keep environment versions consistent across runs (pin package versions in `requirements.txt` for exact replication).
- Save trained models and evaluation metrics to a timestamped directory or via `wandb` artifacts.

## References
- PyTorch RL Tutorial: https://docs.pytorch.org/tutorials/intermediate/reinforcement_q_learning.html
- Gymnasium Docs: https://gymnasium.farama.org
- Experiment tracking and MLOps with Weights & Biases: https://docs.wandb.ai/guides/track/

## Contributing
- Issues and pull requests are welcome. Please keep changes focused and documented in notebooks.

## License
- Educational use intended. If you plan to publish or redistribute, add a proper license file (e.g., MIT) and cite external resources accordingly.
