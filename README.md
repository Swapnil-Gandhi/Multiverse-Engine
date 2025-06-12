<div align="center">
<h1><img src="assets/multiverse-logo.png" height="40px" align="top"/> Multiverse Engine
</h1>

This repository contains the official implementation of **Multiverse Engine**,  which is built up from the [SGLang](https://github.com/sgl-project/sglang) codebase to support inference for **Multiverse Models**. For more details about Multiverse, please refer to our research paper: 
>[**Multiverse: Your Language Models Secretly Decide How to Parallelize and Merge Generation**](https://arxiv.org/abs/2506.09991)


</div>

## 🚀 Installation

To set up the environment, create a new conda environment and then run the provided installation script.

```bash
conda create -n multiverse python=3.11
conda activate multiverse

git clone https://github.com/Multiverse4FM/Multiverse-Engine
cd Multiverse-Engine
bash install.sh
```


## ✨ Quick Start

The usage of Multiverse Engine is the same as the standard SGLang workflow. See `example.py` for a simple use case.

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