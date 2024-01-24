# LLM_entropy

**Table Of Contents**

- [Description](#description)
- [Environment](#environment)
- [Prerequisites](#prerequisites)
- [Running the sample](#running-the-sample)

## Description

This repository is the halfway tensorRT API implementation of the LLaMA decoder.
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

## Running the sample

All implemented components can be found in the `trt_dev` directory, and most of them can directly run with Jupyter Notebook.
For ` .py` in the directory, those are the halfway implementation of library components.
