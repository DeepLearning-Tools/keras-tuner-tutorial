# keras-tuner-tutorial
Hands on tutorial for keras-tuner

This repo aims at introducing hyperparameter tuning through the Keras Tuner library.
It provides a comparison of its different tuners, applied to computer vision through the CIFAR10 dataset.

This is work in progress, all feedback is welcomed.

### Install the project
- Clone the repo
- Create a virtualenv and activate it:
```
virtualenv -p python3 venv
source venv/bin/activate
```
- Install the requirements:
```
pip install requirements.txt
```


### Results

Tasks duration was measured on an RTX 2080 GPU

| Tuner                 | Search time   | Best accuracy (%) |
|-----------------------|---------------|-------------------|
| Random Baseline       | 20min | 72.8             |
| Default Baseline      | 20min | 74.5              |
| Random Search         | 10h 59min  | 76.8              |
| Hyperband             | 10h 0min   | 75.1              |

Increases the worst set of hyperparameters by 10%

### Run the baseline

```
python baseline.py
```

### Run the comparison
Available tuners :

- Random Search
- Hyperband

```
python tuner_comparison.py
```
