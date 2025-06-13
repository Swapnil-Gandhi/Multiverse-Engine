<div align="center">
<h1><img src="assets/multiverse-logo.png" height="40px" align="top"/> Multiverse Engine
</h1>

This repository contains the official implementation of **Multiverse Engine**,  which is built up from the [SGLang](https://github.com/sgl-project/sglang) codebase to support inference for **Multiverse Models**. For more details, please refer to our research paper: 
>[**Multiverse: Your Language Models Secretly Decide How to Parallelize and Merge Generation**](https://arxiv.org/abs/2506.09991)


</div>

## 🚀 Installation

To set up the environment, create a new conda environment and then run the following installation script.

```bash
conda create -n multiverse python=3.11
conda activate multiverse

git clone https://github.com/Multiverse4FM/Multiverse-Engine
cd Multiverse-Engine
bash install.sh
```


## ✨ Quick Start

The usage of Multiverse Engine is identical to the SGLang workflow. See `example.py` for a simple demonstration.

The script accepts the following arguments:
* `--model_path`: The path to the base model on your local machine or from the Hugging Face Hub.
* `--prompts_path`: A path to a JSON file containing a list of prompts.

To run the quick start example:

```bash
python example.py \
  --model_path Multiverse4FM/Multiverse-32B \
  --prompts_dir ./prompt
```

This will load the model and generate responses for each prompt in the specified text file, leveraging the Multiverse capabilities defined for the model.



## 🚧 Potential Issues

We are actively working on addressing the following known issues and areas for improvement:

* [ ]  **KV Cache Eviction Enhancement:**: The eviction feature for KV cache management should be further improved to handle huge batch size requests more robustly and efficiently.
* [ ]  **Excessive Model Splitting**: We are working to prevent crashes that may occur when the Multiverse model is split into an excessive number of partitions.

If you encounter any other failure cases or unexpected behavior not listed above, please don't hesitate to open an issue on GitHub and provide us with the details.

## 📚 References

The Multiverse Engine is built upon and extends the functionalities of the SGLang codebase. This project was developed based on **SGLang commit 357fb2d**.

For more details on SGLang, please refer to their research paper:

```bibtex
@misc{zheng2024sglangefficientexecutionstructured,
      title={SGLang: Efficient Execution of Structured Language Model Programs}, 
      author={Lianmin Zheng and Liangsheng Yin and Zhiqiang Xie and Chuyue Sun and Jeff Huang and Cody Hao Yu and Shiyi Cao and Christos Kozyrakis and Ion Stoica and Joseph E. Gonzalez and Clark Barrett and Ying Sheng},
      year={2024},
      eprint={2312.07104},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={[https://arxiv.org/abs/2312.07104](https://arxiv.org/abs/2312.07104)}, 
}
```