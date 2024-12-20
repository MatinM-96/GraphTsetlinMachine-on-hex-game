# Graph Tsetlin Machine for Hex Game Winner Prediction

This repository contains tools, scripts, and datasets for training and evaluating Graph Tsetlin Machines (GTM) to predict winners in a Hex game. It includes different board configurations, datasets, and training results for various Hex game sizes.

---

## Project Overview

This project aims to predict the winner of a Hex game dataset with high accuracy under the following conditions:

- **At the end of the game**
- **Two moves before the end**
- **Five moves before the end**

The dataset for this project is generated using the `generateData.ipynb` notebook. Due to GitHub storage limitations, the dataset is not included in the repository. You can generate the dataset by running the notebook and use it for the project.

### Note


We have not run the updated code for the 7x7, 10x10, and 13x13 board sizes because we did not have enough time after recent modifications (removal of all comments and unnecessary code). The updated code, which was not run, includes two moves from the start and five moves before the end for the 13x13 board.

---

## Project Structure

```plaintext
.
├── examples/           # Example scripts for various tasks
├── figures/            # Stores generated figures and plots
│   └── ...
├── GraphTsetlinMachine/
│   └── ...             # Contains core GTM implementation
│
├── tools/              # Additional tools and helper scripts
│
├── LICENSE             # License information
├── README.md           # Project description (this file)
├── setup.py            # Setup file for project dependencies
└── generateData.py     # Script to generate Hex game datasets
```

---

## Key Files

### `generateData.py`
A script that generates Hex game datasets. Adjust the game dimensions and the number of games as needed.

### `setup.py`
Script for installing project dependencies.

### `GraphTsetlinMachine/`
Contains the implementation of the Graph Tsetlin Machine (GTM), including the `graphs` and `tm` modules.

---

## Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/MatinM-96/GraphTsetlinMachine-on-hex-game.git
cd GraphTsetlinMachine-on-hex-game
pip install -r requirements.txt
```

---

## Usage

### 1. Generate Hex Game Data

Run the `generateData.py` script to generate custom datasets:

```bash
python generateData.py
```

This will create a CSV file with board configurations and winners.

### 2. Training and Evaluation

Run the GTM training scripts to train on specific datasets:

```bash
python train_gtm.py --dataset datasett/Final13x13.csv
```

---

## Dependencies

- Python 3.8+
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Graph Tsetlin Machine Library (custom)

Install dependencies using:

```bash
pip install -r requirements.txt
```

---
