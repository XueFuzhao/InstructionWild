# Instruction in the Wild: A User-based Instruction Dataset


## Overview

Instruction Tuning is a key component of ChatGPT. OpenAI used their user-based Instruction dataset, but unfortunately, this dataset is not open-sourced. [Self-Instruct](https://github.com/yizhongw/self-instruct) released a small instruction dataset including 175 instructions written by human labors. [Standford Alpaca Team](https://github.com/tatsu-lab/stanford_alpaca) generated 52K instructions by text-de 

Note: This is an ongoing project. We are still collecting and improving our data. We release this dataset as early as possible to speedup our LLM research. We will also release a whitepaper soon.

## Data Release

Our dataset use the same format as [Alpaca](https://github.com/tatsu-lab/stanford_alpaca) for fast and easy usage.
TODO(Zangwei)


## Data Collection

We scrapt over 700 noisy instructions from Twitter and filter out noisy insturctions. We then pick clean insturctions to ensure the high quality
TODO(Zangwei)

## How Good is InstructWild?

[Colossal AI](https://colossalai.org/) used our model to train.

## Authors

This dataset is collected and cleaned by the following authors:

- [Fuzhao Xue](https://xuefuzhao.github.io/)
- [Zangwei Zheng](https://zhengzangw.github.io/)

Both authors are advised by [Prof. Yang You](https://www.comp.nus.edu.sg/~youy/). 

We also acknowledge the valuable suggestions from [Aixin Sun](https://personal.ntu.edu.sg/axsun/), [Tom Young](https://tomyoung903.github.io/).

## Citation

Please cite the repo if you use the data or code in this repo.

```
@misc{alpaca,
  author = {Fuzhao Xue and Zangwei Zheng and Yang You },
  title = {Instruction in the Wild: A User-based Instruction Dataset},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/XueFuzhao/InstructionWild}},
}
```
