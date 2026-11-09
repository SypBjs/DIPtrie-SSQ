# DIPtrie-SSQ

This repository contains the source code and experimental scripts for the paper: 
**"A Mismatch-Enhanced Length Filtering-Based Set Similarity Query Algorithm"** (Under anonymous review).

## 1. Overview

This project implements **DIPtrie-SSQ**, an efficient Set Similarity Query algorithm based on a novel prefix tree structure named **DIPtrie**. It leverages a mismatch-enhanced length filtering technique to accelerate queries on large-scale datasets.

## 2. Environment & Build

The code is written in standard C++11 and has been tested on:
*   **OS**: Ubuntu 24.04.1 LTS
*   **Compiler**: GCC 13.2.0
*   **Hardware**: 4-core CPU, 16 GB memory (Recommended to run full datasets).


## 3. Dataset Preparation

The datasets and their corresponding query sets used in our experiments need to be placed in the directory. 

*   **Dataset files**: `retail.txt`, `kosarak.txt`
*   **Query set files**: `retail_query.txt`, `kosarak_query.txt`

## 4. How to Run

1. Download the code, dataset, and query set.
2. In the `DatasetConfig datasets[]` array in **`main.cpp`**, specify the actual file paths of the dataset (`datafile_path`) and query set (`queryfile_path`) for  `retail` and `kosarak` respectively.
**Step 1: Compile the project**
Run the following commands in the root directory:
```bash
chmod +x compile.sh
./compile.sh
```

Step 2: Execute the program
Run the executable by specifying the dataset (-d) and the threshold (-t, default is 0.6).
# View help
```bash
./bin/DIPtrieSSQ -h
# Run with default threshold (0.6)
./bin/DIPtrieSSQ -d retail
```

