# trt_LLM_decoder

**Table Of Contents**

- [Description](#description)
- [Environment](#environment)
- [Prerequisites](#prerequisites)
- [Running the sample](#running-the-sample)

## Description

This repository is the halfway tensorRT API implementation of the LLaMA decoder.
The purpose of this project is trying to leverage nvidia TensorRT to generate a platform optimized LLaMA implementation.
The work is paused because of the release of [NVIDIA/TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM), a more thorough reimplementation of LLMs.
In TensorRT-LLM, nvidia ported FasterTransformer to TensorRT plugins, resulting a slightly easier reconstruction for users.

## Environment

1. Use `startDocker.sh` to create the torch and TensorRT environment.

2. (Optional) `startJupyterLabOnly.sh` can create a Jupyter Lab environment.

## Prerequisites

1. Upgrade the pip version and install the huggingface/transformers.
    ```bash
    pip3 install --upgrade pip
    pip3 install transformers
    ```
2. Some experiments use the model weight from [baffo32/decapoda-research-llama-7B-hf](https://huggingface.co/baffo32/decapoda-research-llama-7B-hf/tree/main).
    Please download `pytorch_model-00001-of-00033.bin` and store it in `trt_dev/weights`


## Running the sample

All implemented decoder components can be found in the `trt_dev` directory, and most of them can directly run with Jupyter Notebook.
The structure of notebooks is

1. A torch implementation from huggingface as the baseline implementation
2. An tensorRT implementation of the same component
3. Validating the result of both is still in a reasonable error range (typically, within ~1e-4)
4. (Only part of notebooks) A performance comparison

For ` .py` in the directory, those are the halfway implementation of library components.
