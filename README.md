# RLQP: Accelerating Quadratic Optimization with RL

<img src="https://raw.githubusercontent.com/BerkeleyAutomation/rlqp/gh_pages/assets/rlqp-img/conceptual_figure.png?token=AADOZWQXPT5BO5YXHRI7GULA5XWUG">

We demonstrate reinforcement learning can significantly accelerate first-order optimization, outperforming state-of-the-art solvers by up to 3x. RLQP avoids suboptimal heuristics within solvers by tuning the internal parameters of the ADMM algorithm. By decomposing the policy as a multi-agent partially observed problem, RLQP adapts to unseen problem classes and to larger problems than seen during training.

## Getting Started
RLQP is composed of a few submodules, namely to (a) train the RL policy on a specific class of problems (source in `rlqp_train/`) and (b) evaluate the policy on a test problem. Most users will want to start by using RLQP's policy to accelerate optimization of their problems.

### Prerequisites

### Installation (evaluation)
To install the Python package to *evaluate* a pre-trained policy, run:
```
pip install git+https://github.com/berkeleyautomation/rlqp-python.git@55f378e496979bd00e84cea4583ac37bfaa571a9
```

This package contains a pre-trained model which should improve convergence beyond OSQP. The interface is identical to OSQP.

### Installation (training)
Please follow the instructions in the `rlqp_train/` directory to setup and run training code. This code is still in *preview* mode as we work to release features like our TD3 policy.

## Citation
```
@article{ichnowski2021rlqp,
  title={Accelerating Quadratic Optimization with Reinforcement Learning},
  author={Jeffrey Ichnowski, Paras Jain, Bartolomeo Stellato,
    and Goran Banjac, Michael Luo, Francesco Borrelli
    and Joseph E. Gonzalez, Ion Stoica, Ken Goldberg},
  year={2021},
  journal={arXiv preprint}
}
```
