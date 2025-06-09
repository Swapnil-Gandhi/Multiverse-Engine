<div align="center">
<h1><img src="assets/multiverse-logo.png" height="40px" align="top"/> Multiverse Engine
</h1>

This repository contains the official implementation of the **Multiverse Engine**, a modified SGLang <img src="assets/sgl-logo.png" height="20px" align="top" alt="SGLang Logo"/> codebase designed to support the inference of our **Multiverse Models**, as introduced in our paper:


> *Multiverse: Your Language Models Secretly Decide How to Parallelize and Merge Generation*


</div>

## 🚀 Installation

To set up the environment, create a new conda environment and then run the provided installation script.

```bash

conda create -n multiverse python=3.9
conda activate multiverse

git clone https://github.com/Multiverse4FM/Multiverse-Engine
cd multiverse-engine
bash install.sh

```

The install.sh script will install all necessary dependencies from `requirements.txt` and set up the project.


## ✨ Quick Start

The usage of the Multiverse Engine is designed to be identical to the standard SGLang workflow. We provide `example.py` to demonstrate a simple use case.

The script accepts the following arguments:
* `--model_path`: The path to the base model on your local machine or from the Hugging Face Hub.
* `--prompts_path`: A path to a JSON file containing a list of prompts.

To run the quick start example:

```bash
python example.py \
  --model_path  \
  --prompts_path 
```

This will load the model and generate responses for each prompt in the specified text file, leveraging the Multiverse capabilities defined for the model.