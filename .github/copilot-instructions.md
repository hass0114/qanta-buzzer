This repository is a Python project for CS234 reinforcement learning experiments on quiz-bowl style question answering.

## Project overview

- Core modules live in the repository root.
- `config.py` defines the main configuration values and default paths.
- `main.py` is the main entry point for supervised training, PPO training, full runs, and evaluation.
- `environment.py`, `dataset.py`, `model.py`, `train_supervised.py`, `train_ppo.py`, and `metrics.py` contain the main training and evaluation logic.

## Development guidance

- Keep changes minimal and focused on the requested task.
- Prefer updating the existing root-level Python modules instead of introducing new abstractions unless they are clearly necessary.
- Follow the existing style in each file. This repository uses simple module-level scripts and straightforward class-based organization.
- Do not add new dependencies unless they are required for the task.

## Validation

- Install dependencies with `pip install -r requirements.txt`.
- Existing validation scripts are:
  - `python test_imports.py`
  - `python test_csv_loader.py`
- `python main.py --help` shows the supported CLI options for the main training entry point.

## Repository-specific notes

- `requirements.txt` includes heavyweight ML dependencies such as PyTorch and Transformers.
- The first model run may download `t5-large`, so avoid unnecessary execution-heavy changes when working on documentation or configuration tasks.
- There is no existing CI or dedicated lint configuration in the repository, so reuse the current scripts and commands instead of introducing new tooling.
